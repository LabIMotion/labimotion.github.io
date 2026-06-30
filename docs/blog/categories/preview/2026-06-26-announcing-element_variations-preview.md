---
layout: default
title: "(New) Generic Element Variations Editor"
date: 2026-06-26
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260626
categories: [Announcements, Preview]
has_toc: true
description: A Variations tab where each row captures one variation of a generic element.
---

(New) Generic Element Variations Editor
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

The new **Variations** tab on a generic element's detail view gives you an editable grid where each row is one *variation* of the element — a place to record several parameter sets, runs, or conditions side by side. Modelled on Chemotion's **Reaction Variations** and generalized to any generic element, it answers *"I made this several ways — let me capture them all in one place"* without needing a separate template per run.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers, Researchers
>
> **Interface:** Chemotion ELN — Generic Element detail view
{: .info }

- **A row per variation**: Capture multiple runs or conditions of one element in a single editable grid.
- **Choose your columns**: Build the table from the element's own property fields, its segments, plus metadata — **Notes**, **Analyses**, and **Group**.
- **Unit-aware**: For unit-bearing columns, cycle units in the column header; values convert automatically.
- **Fast row building**: Duplicate a row to clone its values, or seed the first row from the element's current values.
- **Per-row analyses & notes**: Link analyses to a variation (or to a specific layer), edit notes, and assign a group.
- **Reorderable & autosaved**: Drag rows and columns to reorder; edits autosave on leaving the tab, and a **"N variations"** badge then appears on the element in the list.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Designers — set up what can be varied

There is no separate per-template switch to author: the Variations tab reads from the element's existing template. What you design upstream is what a user can turn into columns.

- **Property fields** become variation columns when they are an eligible type: `integer`, `number`, `select`, `select-multi`, `system-defined`, `text`, `date`, `datetime`. Other field types are skipped — so design the fields you want users to vary as one of these.
- **Segment fields** are offered too — any segment attached to the element contributes its fields under the **Segments** group in the column picker.
- **Units** ride along for `system-defined` (unit-bearing) fields: the designer's unit set is what users cycle through in the column header.

In short: define the relevant fields and segments on the template; the variations grid exposes them automatically.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Users — record variations

1. Open the generic element → click the **Variations** tab.
2. Click **Select columns** and tick the properties, segments, and metadata (**Notes**, **Analyses**, **Group**) you want as columns.
3. Add rows — each row is a variation. **Duplicate** a row to clone its values as a starting point; you can also seed the first row from the element's current values.
4. Fill in each cell. For unit-bearing columns, click the header to **cycle units** (values convert automatically).
5. Per row you can edit **Notes**, **link analyses** to the variation (or to a specific layer), and assign a **Group**.
6. **Drag** the row handle to reorder variations; **drag** a column header to reorder columns.
7. Edits **autosave** when you leave the tab; a **"N variations"** badge then shows on the element in the list.

Hiding a column that still holds data prompts a **"Hide and clear"** warning so you don't lose values silently. **Remove all** clears the whole table (with confirmation).

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **One record per element.** All variations for an element live in a single record — a `variations` blob (the rows and cell values) and a `layout` blob (visible columns, order, widths) — so the variations travel with the element.
- **Stable column identity.** A property column maps unambiguously back to a template field even across layers; metadata columns use fixed keys (`notes`, `analyses`, `group`).
- **Flexible analyses linking.** Analyses can be linked per row, or to a specific layer within a variation — not just to the whole row.
- **Units convert on the client.** The chosen display unit per column is remembered per user and element, while the saved values stay in the base unit.
- **Groups batch rows.** Sequential and repetition numbering helpers mirror how Reaction Variations replicate sample sets.
- **Autosave seam.** Pending grid edits flush when you switch tabs, marking the element dirty so they persist alongside it.

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
