---
layout: default
title: "(New) Segment Placement & Element-Type Variants"
date: 2026-08-07
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260807
categories: [Preview]
has_toc: true
description: Embed a segment in an element's own tab instead of giving it a tab of its own, and optionally scope it to one element-type variant.
---

(New) Segment Placement & Element-Type Variants
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

Segments used to always get **their own tab**, on every element of their type. Now a segment can instead **embed inside an existing tab** — Properties, or Scheme for reactions — and optionally apply to only **one type variant** of that element.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers, Researchers
>
> **Interface:** Chemotion ELN / Segment Designer, Sample, Reaction and other element pages
{: .info }

- **Embed instead of a new tab**: a segment can render inside the **Properties** tab (Sample, Screen, Wellplate, …) or the **Scheme** tab (Reaction), stacked with a heading, instead of getting its own tab.
- **Narrow to a type variant**: an embedded segment can be scoped to one variant — **Micromolecule**/**Mixture** for samples, **Standard**/**Interaction** for reactions — or left on "all types".
- **Live filtering**: switch an element's type and matching embedded segments appear or disappear immediately — no reload.
- **Data isn't lost**: a segment that no longer matches the current variant is **hidden, not deleted** — its data comes back as soon as the variant matches again.
- **Generic elements unaffected**: generic element segments keep their own tab only; embedding and variants are for built-in elements.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. In the **Segment Designer**, create or edit a segment and set **Assign to Element** to Reaction.
2. Set **Segment Tab** to *Scheme tab*, and optionally **Reaction Type** to *Interaction*.
3. **Save and Release** the segment as usual.
4. Open a reaction of type **Interaction** — the segment now appears stacked inside the **Scheme** tab instead of on its own. Switch the reaction to **Standard** and it disappears; switch back and it's there again, data intact.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **A per-segment choice.** Placement and variant are set per segment template in the Designer, not as a global setting, and travel with the segment's releases.
- **Nothing breaks.** Segments and templates from before this release keep working unchanged, as their own tab.

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
