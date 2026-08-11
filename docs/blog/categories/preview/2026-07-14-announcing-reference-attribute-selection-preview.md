---
layout: default
title: "(New) Reference Attribute Picker"
date: 2026-07-14
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260714
categories: [Preview]
version: 2.4.0-rc
has_toc: true
description: Pick which properties of a linked record show inline on a reference field — see the attributes you care about without opening the linked element.
---

(New) Reference Attribute Picker
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
  version=page.version
%}

Generic records can carry reference fields that link to another record — a linked sample, a linked molecule, and a linked element. With **Reference Attribute Picker**, each reference gets a **list** icon ( <i class="bi bi-card-list"></i> ) that opens a checkbox dialog of the linked record's properties. Tick the ones you care about, press **Apply**, and those attributes render inline on the field — so the form shows exactly the properties you want without ever opening the linked record.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Researchers
>
> **Interface:** Chemotion ELN / Generic Element, Segment, Dataset
{: .info }

- **Inline linked attributes**: Show a linked record's key properties directly on the reference field — no need to open the linked sample or molecule or element to read them.
- **Pick exactly what matters**: A **Select linked element attributes** dialog lists the linked record's properties as checkboxes; tick only the ones relevant to this form.
- **Independent per reference**: Each linked element, linked sample, and linked molecule can be configured separately, each showing its own chosen attributes side by side.
- **Non-destructive**: The attribute picks are a display choice — nothing on the linked record is changed and no data is written.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenarios

### Scenario: Displaying Attributes from Multiple Linked Records

1. **Open a generic element** and go to its **Properties** form; scroll to the **Ref Sample** and **Ref element** fields.
2. **Open the picker**: Click the **list** icon ( <i class="bi bi-card-list"></i> ) next to a reference to open the **Select linked element attributes** dialog.
3. **Tick the properties** you want to display — for a Ref Sample that might be Purity / Real Amount / Density; for a Ref element (cell line) Cell line name / Amount / Passage.
4. **Apply**: The chosen properties appear inline on the field as compact chips.
5. **Repeat** for the other reference — each field keeps its own selection.

(Click the video to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 .text-center }

<div style="display: flex; justify-content: center; margin: 0 0 1.5rem;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-attribute-selection.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-attribute-selection.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 .text-center }

[![Ref Sample and Ref element fields displaying their selected attributes inline as chips](/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-props.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-07-14-reference-attribute-selection-preview/reference-props.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **The selection is a view, not a copy.** You choose which of the linked record's attributes to surface; the values are read from the linked record, so what you see stays in step with the source.
- **Each reference is configured on its own.** Every linked record maintains its own attribute selection, allowing a single form to display different sets of attributes for different references. For example, one form can display a linked sample's Purity and Amount alongside a linked molecule's Molecular Weight and Formula.
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
