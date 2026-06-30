---
layout: default
title: "Version 2.3.0 Public Preview"
date: 2026-06-30
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260630
categories: [Announcements, Preview]
has_toc: true
description: New field types, in-table formulas, system-user selection, generic element variations, and more supported units.
---

Chemotion LabIMotion 2.3.0 in public preview
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

Dear Chemotion LabIMotion users,

Chemotion LabIMotion 2.3.0 is now available for public preview!

This preview highlights the upcoming enhancements and provides early access to new functionality planned for the next official release. It delivers improvements across **new field types**, **in-table formulas**, **system-user selection**, **generic element variations**, **user-view refinements**, and **more supported units**.

Each highlight below links to a dedicated deep-dive post.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Highlights

### 🔢 New Field Types

Three new field types expand how data is captured in templates:

- **Number** — a dedicated numeric field with configurable decimals, range constraints, and scientific notation; also available as a table column. → [Number Field Type](/blog/categories/preview/2026-04-15-announcing-number_field_type-preview)
- **Ontology Selection** — pick a term from a controlled ontology tree instead of typing free text, and use it as a restriction source. → [Ontology Selection Field Type](/blog/categories/preview/2026-06-30-announcing-ontology_select-preview)
- **Select (Multiple)** — choose several options at once, in both layer fields and table columns, with pick-order preserved. → [Select (Multiple) Field & Table Renderer](/blog/categories/preview/2026-06-29-announcing-select_multi-preview)

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 🧮 Formulas in Tables

- **Formula-Field column** — a read-only table column that calculates each row's value from the other columns in that same row (e.g. *Mass × Amount*), with unit-safe results and values stored for export. → [Formula-Field Table Column](/blog/categories/preview/2026-06-28-announcing-formula_column-preview)

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 👥 System User Selection

- Point an ordinary **Select** or **Select (Multiple)** field at the host's real user directory instead of a fixed option list — users search and pick real people, only ids are stored, and names stay current. → [System User Selection](/blog/categories/preview/2026-06-27-announcing-system_user_select-preview)

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 🔬 Generic Element Variations

- A new **Variations** tab on a generic element, where each row captures one variation (run / condition) of the element. Columns are drawn from the element's property fields, segments, and metadata, and the table is saved per element. → [Generic Element Variations Editor](/blog/categories/preview/2026-06-26-announcing-element_variations-preview)

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 🏷️ User-View Enhancements

- **Custom dynamic layer name** shown in *Arrange layers* and the *Overview Map*. → [Dynamic Layer Name](/blog/categories/preview/2026-01-13-announcing-dynamic_layer_name-preview)
- **Template version & identifier** surfaced in the user view, with a *Show more* control for the revisions list.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 📏 More Supported Units

LabIMotion keeps expanding the units available for **System-Defined** fields, and 2.3.0 adds even more. Browse the full list here: [Supported Units for System-Defined Field](https://github.com/LabIMotion/labimotion/wiki/Supported-Units-for-System-Defined-Field).

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

*Note: These features are currently in preview and may undergo further refinements based on user feedback.*

---

## How to Participate in the Preview

{: .note }
>
> 1. 🖥️ **Visit the Test Instance:**
>    [labimotion-stage.ibcs.kit.edu](https://labimotion-stage.ibcs.kit.edu/home)
>
> 2. 🔍 **Explore the New Features:**
>    Try out the enhancements and evaluate how they support your work.
>
> 3. ❤️ **Provide Feedback:**
>    Please share your comments in our [GitHub Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/87).

We appreciate your participation and look forward to your feedback.

Thank you!

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
