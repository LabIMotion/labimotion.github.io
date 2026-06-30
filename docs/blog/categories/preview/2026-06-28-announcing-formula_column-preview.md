---
layout: default
title: "(New) Formula-Field Table Column"
date: 2026-06-28
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260628
categories: [Announcements, Preview]
has_toc: true
description: A read-only table column that calculates each row's value from the other columns.
---

(New) Formula-Field Table Column
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

The new **Formula-Field** column calculates a value for every row of a table from the other columns in that same row — for example *Mass × Amount*. It works like the layer-level formula field, scoped to a single table row, and recalculates automatically as the data changes.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers, Researchers
>
> **Interface:** Chemotion ELN / Generic Template Designer
{: .info }

- **Per-row calculation**: Each row's formula value is derived from that row's other columns, updated automatically.
- **Read-only cells**: No one types into a formula cell — it recalculates on its own whenever its inputs change.
- **Number & System-Defined operands**: Formulas use **Number** and **System-Defined** (unit-bearing) columns of the same table; any other column counts as `0`, so formulas can never reference each other in a loop.
- **Stable references**: A formula tracks the column itself, not its heading text — so renaming a column never breaks it.
- **Unit-safe results**: A pinned default unit keeps results consistent no matter which unit a viewer is displaying.
- **Stored, not just shown**: Computed values are written back into the saved table data, so exports get the real numbers with no extra calculation.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Designers — building a formula column

1. In your table, add a column and set its **Column Type** to **Formula-Field**.
2. A **Formula** button appears on that column. Click it to open the formula editor.
3. The editor lists the other columns with their **Id**, **Heading**, **Type**, and a short **abbreviation** you use to refer to each one (e.g. `m` for *Mass*, `a` for *Amount*). Abbreviations are auto-suggested from the heading and can be renamed. Eligible columns (Number / System-Defined) are editable; ineligible columns are greyed out and labelled *"counts as 0"*.
4. Type the **Formula** using those abbreviations and standard math operators — e.g. `m * a` or `(a + b) / 2`.
5. Set the **Decimal** precision (the maximum number of decimal places shown).
6. Click **Save**. The **Formula** button becomes highlighted, and hovering it shows the saved formula.

**Validation and warnings**

- A **duplicate or invalid abbreviation** must be fixed before you can save (shown as an error).
- An **unknown name** in the formula, a reference to a **retyped** column, or a reference to a **deleted** column are shown as **warnings** — they don't block saving.

**Good to know**

- **Renaming a column heading is safe** — the formula keeps working because it tracks the column itself, not its heading text.
- If you change an operand column to an **ineligible type**, the formula treats it as `0` until you switch the type back — then it reconnects automatically.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Designers — choosing the unit a formula calculates in

When a formula uses a **System-Defined** (unit-bearing) column, the result must not change just because someone *displays* the value in a different unit. To guarantee this, you pin a **default unit** for the column, and the formula always calculates in that unit.

- For a System-Defined column, use the **Default Unit** control in the table's work area to choose the unit.
- Existing values are converted automatically when you change the unit (e.g. `1000 g` becomes `1 kg` — values are never silently mislabelled). If the change switches to a different kind of quantity, the now-meaningless value is cleared.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Users — entering data

- A formula cell is **read-only** and right-aligned. It recalculates **instantly** whenever you edit any column it depends on.
- **Adding a row** calculates its formula immediately.
- **Empty inputs** count as `0`. If a formula was written incorrectly, the cell shows an **error message** instead of a number.
- The **decimal** setting is a maximum — trailing zeros are not shown (e.g. `2.50` displays as `2.5`).
- **Units stay consistent:** changing the unit you *view* a System-Defined value in does not change any formula result. Hover the small **information icon** on a System-Defined column header to see its default unit; a formula column's tooltip notes that it uses the referenced columns' default units.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **Stable references.** A formula stores the *identity* of each column it uses, not its heading text, so renaming a heading never breaks a formula.
- **A pinned base unit keeps results stable.** Before a System-Defined operand is used, its value is normalized to the column's pinned **default unit**, so the result is always expressed in that unit — unaffected by the unit a viewer happens to be displaying.
- **Results are stored, not just shown.** Each computed value is written back into the saved table data, so exports and server-side reads get the real numbers. Editing a cell, switching a cell's unit, adding or removing a row, or reloading the template all trigger a recompute so the stored values stay correct.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

*Note: This feature is currently in preview and may undergo further refinements based on user feedback.*

---

## 🚀 How to Participate in the Preview

Follow these steps to explore the new features and share your insight:

{: .note }
> 1. 🖥️ **Visit the Staging Instance**<br>
> Access the preview environment at: [labimotion-stage.ibcs.kit.edu](https://labimotion-stage.ibcs.kit.edu/home)
>
> 2. 🔍 **Explore and Test**<br>
> Try out the enhancements — see how they fit your workflow.
>
> 3. ❤️ **Your Feedback Matters**<br>
> Share your comments or report any issues in our [GitHub Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/67).

We appreciate your help in testing these new features!

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
