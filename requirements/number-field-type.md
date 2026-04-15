# Feature Specification: Number Field Type

## 1. Background

The system supports multiple field types via `import { FieldTypes } from 'generic-ui-core';`, such as `text`, `date`, `select`, and `integer`. The `integer` type is limited and does not satisfy increasing user requirements for floating-point support, configurable decimal precision, and min/max constraints. The field type `number` (`FieldTypes.F_NUMBER`) replaces it.

---

## 2. Objectives

- Introduce `number` (`FieldTypes.F_NUMBER`) for Designer template configuration
- Replace `integer` with `number`; treat `integer` as `number` with `decimals = 0`
- Provide flexible configuration for numeric input (decimals, min, max)
- Ensure proper validation and clamping based on designer-defined constraints
- Support scientific notation (e.g., `1e10`)

---

## 3. Scope

### In Scope
- Designer configuration UI (decimals, min, max)
- User input validation and display formatting
- Scientific notation support
- Decimal precision enforcement

### Out of Scope
- Automatic migration of existing data
- Thousand separator handling

---

## 4. Functional Requirements

### 4.1 Field Type Definition

- `integer` is removed from the designer field type dropdown
- `integer` type in existing templates is **automatically migrated to `number`** (`numeric: { decimals: 0, min: '', max: '' }`) when the template loads in the designer (`Template.js` via `migrateIntegerFields()`) and when saved (`handleSaveSorting`)
- Both `integer` and `number` use the same rendering code path (`GenPropertiesNumber`); `GenInterface.js` also handles both in a single code path using `parseNumberInput`

---

### 4.2 Designer Configuration

Entry UI: `ElementField.js`

Number-specific config is stored in a nested `numeric` object on the field:

```json
{ "type": "number", "field": "qty", "numeric": { "decimals": 2, "min": 0, "max": 100 } }
```

| Property | Type | Behaviour |
|---|---|---|
| `numeric.decimals` | integer ≥ 0, optional | Max decimal places. Defaults to `0` (shown in UI). Cleared → reset to `0` silently. Float (e.g. `2.5`) or negative → truncated/clamped to nearest valid int + warning. |
| `numeric.min` | float, optional | Lower bound (inclusive). Unset/cleared/non-numeric → stored as `''` → no constraint. Value with more decimal places than `decimals` → rounded to `decimals` precision + warning. |
| `numeric.max` | float, optional | Upper bound (inclusive). Unset/cleared/non-numeric → stored as `''` → no constraint. Value with more decimal places than `decimals` → rounded to `decimals` precision + warning. |

> `allowNegative` is not needed — `min` can enforce positivity.

#### Input UX
- All three fields use `type="text"` inputs (`NumberInputField` component)
- Raw text is preserved while typing — no live parsing
- On `onBlur`: value is parsed and coerced; invalid/cleared → reset to default (`0` for decimals, `''` for min/max)
- This prevents mid-entry interruption (e.g., typing `1.5` would break at `1.` with live parsing)

#### Decimals Validation on Blur
- Cleared / empty → reset to `0` silently
- Float value (e.g. `2.5`) → truncated to `2`, warning: `"Invalid decimals for "[field]" — must be a non-negative integer. Reset to 2."`
- Negative (e.g. `-2`) → reset to `0`, same warning

#### Min/Max Precision Normalization on Blur
- If `min` or `max` has more decimal places than `decimals` allows, the value is rounded using the same `applyPrecision` logic as user input
- Comparison uses `String()` representation to avoid JS float false-positives
- If rounded value differs from entered value → warning: `"Min/Max rounded to [X] for "[field]" to match decimals precision ([d])."`
- If value already fits the precision → stored silently, no warning

#### Type Change Cleanup
- Switching away from `number`/`integer` → the entire `numeric` object and `value` are **deleted** from the field
- A **dynamic warning notification** (`alert-warning`, title: `"Warning"`) is emitted listing only what was actually cleared:
  - E.g. `"Field "qty" type changed: default value and display name reference were cleared."`
  - Items included: `"default value"` (if value was set), `"display name reference"` (if `label_fields` referenced the field), `"restrictions"` (if any `metadata.restrict` entries referenced the field)
  - Silent success if nothing was actually cleared
- Switching `number` ↔ `integer` → all props (including `value`) are **preserved** (same family)
- Switching away from `formula-field` → `formula`, `decimal` deleted
- Switching away from `text`/`number`/`integer` to other types → `placeholder`, `required`, `readonly` deleted

#### Constraint Change — Value Invalidation
When a designer changes `decimals`, `min`, or `max` and the field already has a value (e.g. entered via Preview):
- The stored value is checked against the **new** constraints immediately
- If the value no longer satisfies the new constraints → `value` is cleared to `''` automatically
- A **warning notification** (`alert-warning`, title: `"Warning"`) is shown: `"Default value cleared for "[field]" — it falls outside the updated constraints."`
- This prevents legacy/stale values from silently persisting in violation of updated constraints

#### Constraint Conflict — min > max
When a designer enters a `min` or `max` value that creates an impossible range:
- The **just-entered value** is cleared back to `''` (the other constraint is preserved)
- A **warning notification** (`alert-warning`, title: `"Warning"`) is shown: `"Invalid constraint for "[field]" — min cannot be greater than max."`
- `min === max` is allowed (valid single-point range)
- Uses `isMinMaxValid(min, max)` helper in `numberUtils.js`
- Note: min/max precision normalization (see above) runs **before** the min > max guard, so the rounded value is what gets checked

---

### 4.3 User Input Behavior

Entry UI: `GenInterface.js` / `GenPropertiesFields.js` (`GenPropertiesNumber`)

- Renders as `type="text"` (not `type="number"`) for controlled formatting
- Accepts standard decimal notation (`123.45`) and scientific notation (`1e10`, `1.2e-3`)
- Accepts both `.` and `,` as decimal separators; normalized to `.` before processing
- Displays a muted hint below the field showing active constraints, e.g. `(dec: 2, min: 0, max: 100)` — only shown when `f_obj.numeric` is set; `dec` always shown (even when `0`); `min`/`max` only shown when non-empty

#### Input UX (on `onBlur`)
1. Normalize `,` → `.`
2. Parse with `mathjs` BigNumber
3. Round to `decimals` places (`''` resolves to `0`)
4. Clamp to `max` if set and value exceeds it
5. Clamp to `min` if set and value is below it
6. Store as JSON number; display formatted via `numeral`
7. Invalid or cleared input → store `''` (field appears empty)

Users can always clear the field — it stores `''`, never forces `0`.

---

### 4.4 Validation Rules

#### Libraries
- **`mathjs`** (existing dependency) — BigNumber parsing, rounding, min/max comparison
- **`numeral`** (existing dependency) — display formatting only
- No new dependencies required

#### On Blur Summary

| Field | Valid input | Invalid / cleared |
|---|---|---|
| `numeric.decimals` | integer ≥ 0 → stored as-is | cleared → `0` silently; float/negative → truncated/clamped to nearest valid int + warning |
| `numeric.min` / `numeric.max` | valid float → rounded to `decimals` precision if needed + warning; stored | cleared/non-numeric → `''` (no constraint applied) |
| user `value` | round → clamp → stored as JSON number | `''` |

#### On Submission (`isValidated`)
- Required field (`F_TEXT`/`F_INTEGER`) with `''` → **invalid**
- Any `F_NUMBER` field with a **non-empty** value that violates current constraints (`numeric.decimals`/`numeric.min`/`numeric.max`) → **invalid**, blocks save
- `F_NUMBER` field with empty value (`''`) → **valid** (user chose not to fill it in)
- Constraint validation is independent of the `required` flag — there is no "required" setting for `number` fields in the designer

> **Why `''` not `0`:** Preserves the distinction between "user cleared the field" and "user entered zero". Ensures required-field validation works, and blank `min`/`max` truly means no constraint.

---

### 4.5 Decimal Separator Handling

- Storage always uses `.`
- Input accepts `.` or `,`; normalized before validation
- Multiple or mixed separators → rejected (treated as invalid)
- Thousand separators not supported

---

### 4.6 Scientific Notation Support

- Parsed by `mathjs` BigNumber natively
- Decimal precision enforced after conversion
- Example: `decimals = 2`, input `1e-3` → `0.001` → rounded to `0.00`

---

## 5. Forward Compatibility — Template Import

### 5.1 Problem

Three import paths allow designers to bring templates into the system:

| Path | Handler |
|---|---|
| "Import template into Work Area" | `handleTemplateUploading` |
| "Import an element and its template" | `handleKlassUploading` |
| "Fetch from LabIMotion Hub" | Server-side (`ExternalManager`) — out of scope |

A template authored on a **newer system** (with `number` field type) may be imported into an **older system** that does not know `number`. Without a safety net, the older system either silently renders a blank field or rejects the template at schema validation.

### 5.2 Solution — `updateUnsupports` on Import

`updateUnsupports(layer, genericType)` in `remodel-handler.js` iterates all fields in a layer and downgrades any type not in the current system's supported list (`BaseFieldTypes` / `FieldBase` / `ElementBase`) to `F_TEXT`.

**Applied at import time:**
- `handleTemplateUploading`: runs `updateUnsupports` on all layers **before schema validation**, so unknown types are cleaned up and the template passes cleanly
- `handleKlassUploading`: runs `updateUnsupports` on all layers after klass/input validation succeeds

**Result:** A `number` field imported into an old system becomes a `text` field — no data loss, no crash. When the old system is upgraded, the template can be re-imported and the field type updated by the designer.

### 5.3 Scope Note

The "Fetch from LabIMotion Hub" path calls `ExternalManager.saveTemplate` which is server-side and outside this library. The server is responsible for applying the same downgrade logic when syncing hub templates.

---

## 6. Non-Functional Requirements

- **Consistency**: validation rules consistent across frontend and backend
- **Performance**: no noticeable lag from validation
- **Backward Compatibility**: existing `integer` fields remain functional; no regressions

---

## 7. Migration Strategy

- `integer` type is **no longer available** in the designer dropdown
- Existing templates with `integer` fields are auto-converted to `number` with `decimals=0`, `min=''`, `max=''` when loaded in the designer — no manual migration needed
- If designers save the template, the conversion is persisted permanently
- In `GenInterface.js` (user input), `integer` fields are still supported for backward compatibility and use `decimals=0` with no constraints

---

## 8. Technical Notes

- Valid user values stored as JSON numbers (e.g., `value: 3.5`); unset stored as `''`
- `resolveDecimals(val)` — normalises decimals config: `''`/null/undefined/negative → `0`
- `parseNumberInput(val, decimals, {min, max})` — returns `null` for invalid/empty input; also used for min/max precision normalization (no constraints passed, only rounding)
- `GenPropertiesNumber` uses `useState` to hold raw text while focused; parses only on blur; shows muted constraint hint `(dec: N, min: X, max: Y)` when `numeric` is set
- `NumberInputField` in `Fields.js` is a proper React component (PascalCase) to allow `useState` per Rules of Hooks; decimals field always shows effective value (`0` when unset) via `resolveDecimals`
- Type-change cleanup uses `delete` (not `= undefined`) to fully remove props from the field object
- min/max precision normalization uses `String(rounded) !== String(value)` for comparison to avoid JS float false-positives

---

## 9. Acceptance Criteria

### Designer
- [x] Can create a `number` field and configure `decimals`, `min`, `max`
- [x] `integer` field type removed from designer dropdown
- [x] Existing `integer` fields auto-migrated to `number` (decimals=0) on template load
- [x] Typing in config fields is not interrupted by live parsing
- [x] Clearing `decimals` → reset to `0` silently; float/negative decimals → truncated to nearest valid int + warning
- [x] Non-numeric min/max → `''` on blur
- [x] min/max with more decimal places than `decimals` → rounded to decimals precision + warning
- [x] User-facing hint `(dec: N, min: X, max: Y)` shown below number field when `numeric` config is set
- [x] Configuration persisted correctly
- [x] Type-specific props cleaned up when switching field type
- [x] Dynamic warning when type changes removes data (default value, display name ref, restrictions) — only cleared items listed
- [x] Switching away from `number`/`integer` with no data removed → silent success (no warning)
- [x] Changing constraints that invalidate an existing value → value cleared + warning with "Default value cleared for…" message
- [x] Setting min > max → just-entered value cleared + warning "min cannot be greater than max"; min = max allowed

### User
- [x] Input not interrupted mid-typing; formatting only on blur
- [x] Decimal precision enforced (auto-rounded)
- [x] Out-of-range values clamped to max/min
- [x] Scientific notation accepted
- [x] Both `.` and `,` accepted
- [x] Invalid/cleared input stores `''` (not `0`)
- [x] Field can always be cleared
- [x] Out-of-range stored value (e.g. after template update) shown with red border + error message

### System
- [x] Required `number` field with `''` value fails validation
- [x] Any F_NUMBER field with non-empty value violating constraints blocks save
- [x] Valid values stored as JSON numbers
- [x] `integer` fields remain functional
- [x] No regression in other field types
- [x] Non-type-specific field properties (formula, decimal, label, placeholder, etc.) saved correctly via switch `default` case

### Import Compatibility
- [x] Template import ("Import template into Work Area") downgrades unknown field types to `text`
- [x] Element+template import ("Import an element and its template") downgrades unknown field types to `text`
- [x] Known/supported field types (including `number`) are preserved on import
- [x] Downgrade happens before schema validation so import succeeds cleanly

---

## 10. Implementation Summary

### Core Utility
`src/utils/numberUtils.js` — `resolveDecimals`, `normalizeDecimalSeparator`, `parseDecimal`, `parseNumberInput`, `validateNumberValue`, `isNumberFieldValid`, `isMinMaxValid`, `buildNumeralFormat`, `formatNumberDisplay`

### Files Modified
| File | Change |
|---|---|
| `src/components/elements/BaseFieldTypes.js` | F_INTEGER removed from dropdown; F_NUMBER only |
| `src/components/fields/GenProperties.js` | `case FieldTypes.F_NUMBER` routing added |
| `src/components/fields/GenPropertiesFields.js` | `GenPropertiesNumber` — local state, blur-only parse/format; `isInvalid` + error when value violates constraints; muted hint showing active constraints `(dec: N, min: X, max: Y)`; reads from `f_obj.numeric` |
| `src/components/elements/Fields.js` | `NumberInputField` — decimals field always shows resolved value (`0` if unset) via `resolveDecimals`; min/max show `''` when unset |
| `src/components/elements/ElementField.js` | F_NUMBER config UI; raw input passed through to action-handler (no silent coercion) |
| `src/components/details/GenInterface.js` | F_NUMBER + F_INTEGER both use `parseNumberInput`; F_INTEGER safety net uses `{ min: '', max: '' }`; reads from `fieldObj.numeric` |
| `src/components/layers/GenPropertiesLayer.js` | `f.value ?? ''` (fixes zero display) |
| `src/models/ElementFactory.js` | F_NUMBER: blocks save for any non-empty value violating `f.numeric` constraints |
| `src/utils/template/remodel-handler.js` | F_NUMBER/F_INTEGER: uses `parseNumberInput` (respects B's `numeric.decimals/min/max`); leaves B's template default if conversion fails |
| `src/utils/template/sorting-handler.js` | `migrateIntegerFields(element, propKey='properties_template')` — writes `fd.numeric = { decimals, min, max }`; flexible propKey param |
| `src/utils/template/action-handler.js` | Type-change cleanup: `delete fieldObj.numeric`; initializes `numeric: { decimals: 0, min: '', max: '' }` when switching to `number`/`integer`; decimals validation with warning; min/max precision normalization with warning; min > max guard; default value invalidation on constraint change; `default` case restored; `updateUnsupports` on import |
| `src/utils/template/designer-message.js` | `notifyWarning()` added (lvl: 'warning') |
| `src/components/designer/template/Template.js` | Calls `migrateIntegerFields()` on template load |
| `src/components/designer/template/TemplateBar.js` | Renders `alert-warning` for `lvl === 'warning'` notifications |

---

## 11. Decisions Log

| Question | Decision |
|---|---|
| Display formatting: now or later? | Now |
| Exceed `decimals`: reject or round? | Auto-round |
| Out-of-range: reject or clamp? | Clamp to min/max |
| Invalid/cleared input: `0` or `''`? | `''` for min/max; `0` for decimals (shown in designer UI, no ambiguity) |
| Libraries? | `mathjs` (validation/rounding) + `numeral` (display); no new deps |
| `integer` and `number` same code path? | Yes; `integer` = `number` with `decimals = 0`; F_INTEGER removed from dropdown; auto-migrated on template load |
| Arbitrary precision needed? | No |
| Type-change prop cleanup? | Yes — `delete fieldObj.numeric` (single delete); includes `value` when switching away from `number`/`integer` |
| Type-change warning? | Dynamic: lists only what was actually cleared (`default value`, `display name reference`, `restrictions`); silent if nothing cleared |
| Constraint-change warning message? | Title: `"Warning"`, message: `"Default value cleared for "[field]" — it falls outside the updated constraints."` |
| Legacy value after constraint change? | Cleared automatically + warning shown to designer; user runtime value shows red border + blocks save |
| min > max? | Just-entered value cleared to `''` + warning; `min = max` allowed; uses `isMinMaxValid()` in `numberUtils.js` |
| Invalid decimals (float/negative)? | Truncated/clamped to nearest valid int + warning; cleared → `0` silently |
| min/max precision vs decimals? | Rounded using `parseNumberInput` (same as user input); warning shown if value changed; comparison via `String()` to avoid float false-positives |
| Constraint hint for users? | Muted text `(dec: N, min: X, max: Y)` rendered below number input; always shows `dec`; omits min/max when empty |
| Template import with unknown field types? | `updateUnsupports` applied before schema validation; unknown types downgraded to `text`; `number` preserved on current system |
| `numeric` nested object? | Yes — `decimals`, `min`, `max` moved to `field.numeric = { decimals, min, max }` for clean namespacing; no data migration risk (new field type, no existing stored data) |
