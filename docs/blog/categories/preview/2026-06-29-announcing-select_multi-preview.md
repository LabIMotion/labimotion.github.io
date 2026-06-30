---
layout: default
title: "(New) Select (Multiple) Field & Table Renderer"
date: 2026-06-29
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260629
categories: [Announcements, Preview]
has_toc: true
description: Pick several options from a select list at once — in layer fields and table columns.
---

(New) Select (Multiple) Field & Table Renderer
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

The **Select (Multiple)** field works like an ordinary select field, except users can choose **more than one** option. It is available both as a **layer field** and as a **table column**, and it remembers selections in the exact order the user picked them.

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

- **Multiple picks**: Choose several options from one select list, instead of being limited to a single value.
- **Two homes, one behaviour**: The same control renders as a layer field and as a table cell, so the experience is identical in both.
- **Order preserved**: Selections are stored and shown in the order they were picked — not re-sorted by the option list.
- **Compact display**: The first **2** picks show inline as chips; the rest collapse into a **`+N`** button that opens the full list in a popover for review and removal.
- **Self-healing data**: If an option (or an entire list) is later deleted, stored picks that reference what's gone are cleaned up automatically — no dangling values left behind.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Designers — adding a Select (Multiple) field or column

1. Add a field — or, in a table, add a column — and set its type to **Select (Multiple)**.
2. Point its **option source** at a select list (the same select lists single-select fields use). The field or column then offers every option from that list.
3. **Good to know — automatic cleanup.** If you later delete an option from the list, or delete the whole list, any already-stored picks that reference what's gone are removed automatically, so saved data never points at options that no longer exist.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Users — choosing options

- Click the field or cell to open the dropdown, then click each option you want. Re-open and click again to add or change picks; use **clear-all** to empty it.
- Chosen options appear as **chips**. To keep the layout compact, the first **2** picks show inline and the rest collapse into a **`+N`** button — click it to see the full list in a popover and remove individual items there.
- The chips stay in the **order you selected them**.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **One control, two homes.** The same multi-select control renders in a layer field and in a table cell, so the experience is consistent everywhere.
- **Picked order is the stored order.** The value is the list of picks in selection order; the display rebuilds the chips from that stored order rather than re-sorting by the option list.
- **Compact by default.** Two chips show inline and the remainder collapse behind a `+N` popover, so dense layouts and table rows stay readable.
- **Self-healing data.** When an option or an entire list is removed, stored picks are filtered against the current options, so a template change never leaves dangling values behind.

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
> Share your comments or report any issues in our [GitHub Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/87).

We appreciate your help in testing these new features!

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
