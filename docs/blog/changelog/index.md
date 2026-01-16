---
layout: default
title: Changelog
parent: Blog
nav_order: 3
---

# Changelog

## [next release]

### Features and Enhancements
- **Dynamic Layer Display Names** feature.[(blog)]({% link blog/categories/preview/2026-01-13-announcing-dynamic_layer_name-preview.md %}).
- **Group layers** feature: Layer grouping to manage multiple layers as a single unit.[(blog)]({% link blog/categories/preview/2026-01-07-announcing-layer_grouping-preview.md %}).
- Set restriction values based on field type and assignment.
- New Restriction Settings UI.
- Default information feature in Generic Datasets.
- Enhanced saving validation for Generic Elements to consider field visibility.
- Default reference element information feature in Generic Datasets.
- Template submission support.
- Contextual information and identifiers for Generic Datasets.
- Support for linking Samples in Generic Segments.
- Resizable Work Area.
- SMILES as the default output in **Export table data** functionality when linked Samples exist.
- (UI) Dropdowns automatically flip direction based on available space.
- (UI) Updated unit button size to *small*.
- **Export table data** to XLSX format feature.
- Element associations in Generic Datasets.
- System Units: Pressure, Power, and Volume (Electrochemical and Material Science).
- Sample associations in Generic Datasets.
- Added links to textual descriptions.
- Extended Generic Element identifier to 10 characters.
- Improved color selection UI for layer attributes.
- Sorted element association lists for better usability.
- Edit Mode for data exchange.
- Added controls to support the MoleculeArchive platform.
- Version information summary.
- Column reordering via UI in Designer table fields.
- (UI) Added search icon to **Quick Filter**.
- (UI) Moved **Quick Filter** to the top of the page.
- Display template version information in the MyDB view.
- Introduced components with built-in unit conversion utilities for developers.
- Improved layer collapse/expand button style.

### Bug Fixes
- Fixed an issue where adding a Reaction to a Generic Segment failed after the UI refactor.
- Fixed layer styles being overridden by external styles.
- Fixed `useDnD` not being recognized.
- Fixed creation issue (database ancestry changes) caused by library upgrade.
- Fixed default values not applying correctly for Multiple Selection fields in the Designer.
- Fixed the text-formula field not working in the Designer.
- Fixed intermittent disappearance of the scrollbar on the Designer page.
- Fixed datetime field styles being overridden by external wrappers.
- Fixed **Quick Filter** reset not working.
- Fixed input losing focus after entering one character in Designer select fields.
- Fixed incorrect ordering numbers on version list.

### Chores
- Renamed:
  - Drag Element → Link Element
  - Drag Molecule → Link Molecule
  - Drag Sample → Link Sample
- Refactored button implementation by introducing a shared tooltip button component.
- Refactored the revision modal.
- Added index for efficient querying.
- Added safer parsing when converting text to links.
- Removed unused properties, styles and components.
- Removed custom datepicker styles due to a library upgrade.
- Migrated utility functions to `pureUtils` for better organization.
- Node.js version upgrade.
- Dependency upgrades and test coverage improvements.

For more details, see the [Discussions](https://github.com/LabIMotion/labimotion/discussions).

## Current Version
- [2.0.0](https://github.com/LabIMotion/labimotion/blob/main/CHANGELOG.md#200)

## Previous Versions
- [Full Changelog](https://github.com/LabIMotion/labimotion/blob/main/CHANGELOG.md)
