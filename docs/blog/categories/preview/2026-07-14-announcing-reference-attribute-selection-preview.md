---
layout: default
title: "(New) Reference Attribute Selection"
date: 2026-07-14
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260714
categories: [Announcements, Preview]
has_toc: true
description: Pick which properties of a linked record show inline on a reference field — see the attributes you care about without opening the linked element.
---

(New) Reference Attribute Selection
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

Generic elements can carry **reference fields** that link to another record — a **Ref Sample** (a linked sample) and a **Ref element** (for example a linked cell line). With **Reference Attribute Selection**, each reference gets a **list** icon that opens a checkbox dialog of the linked record's properties. Tick the ones you care about, press **Apply**, and those attributes render inline on the field — so the form shows exactly the properties you want without ever opening the linked record.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Researchers
>
> **Interface:** Chemotion ELN / Generic Element: Properties form — reference fields
{: .info }

- **Inline linked attributes**: Show a linked record's key properties directly on the reference field — no need to open the linked sample or element to read them.
- **Pick exactly what matters**: A **Select linked element attributes** dialog lists the linked record's properties as checkboxes; tick only the ones relevant to this form.
- **Independent per reference**: **Ref Sample** and **Ref element** are configured separately, each showing its own chosen attributes side by side.
- **Non-destructive**: The attribute picks are a display choice — nothing on the linked record is changed and no data is written.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Using it

1. **Open a generic element** and go to its **Properties** form; scroll to the **Ref Sample** and **Ref element** fields.
2. **Open the picker**: Click the **list** icon next to a reference to open the **Select linked element attributes** dialog.
3. **Tick the properties** you want to display — for a Ref Sample that might be **Purity / Real Amount / Density**; for a Ref element (cell line) **Cell line name / Amount / Passage**.
4. **Apply**: The chosen properties appear inline on the field as compact chips.
5. **Repeat** for the other reference — each field keeps its own selection.

(Click the video to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-attribute-selection.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-attribute-selection.mp4" type="video/mp4">
    <source src="/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-attribute-selection.webm" type="video/webm">
    Your browser does not support the video tag.
  </video>
</div>

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Ref Sample and Ref element fields displaying their selected attributes inline as chips](/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-props.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-props.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **The selection is a view, not a copy.** You choose which of the linked record's attributes to surface; the values are read from the linked record, so what you see stays in step with the source.
- **Each reference is configured on its own.** Ref Sample and Ref element hold separate attribute selections, so one form can show a sample's purity and amount next to a cell line's passage.
- **Nothing is persisted to the link.** The picker only controls what displays — it never writes to or alters the linked element.

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
> Share your comments or report any issues in our [GitHub Discussions](https://github.com/LabIMotion/labimotion/discussions).

We appreciate your help in testing these new features!

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
