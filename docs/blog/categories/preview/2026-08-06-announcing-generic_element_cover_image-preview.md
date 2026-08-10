---
layout: default
title: "(New) Cover Image for Generic Elements"
date: 2026-08-06
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260806
categories: [Preview]
has_toc: true
description: Give a generic element a cover image built from its own attachments and analyses, shown right above its segments.
---

(New) Cover Image for Generic Elements
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

Generic elements can now show a **cover image** — a fixed-size strip of pictures rendered above the element's segments, built from images you already have on the element. No separate upload: you pick from its existing **Attachments** and **Analyses**.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers, Researchers
>
> **Interface:** Chemotion ELN / Generic Element detail view
{: .info }

- **Cover image area**: A fixed-size image display sits above an element's segments, paging through the images you selected.
- **Designer opt-in**: Template Designers switch Cover Image on or off per element klass, alongside the other Layer Function Controls.
- **Pick from what's already there**: Choose images from the element's own **Attachments** and **Analyses** — nothing new to upload.
- **Order it your way**: Move images between a Candidate List and a Selected list, and reorder the selected ones.
- **Off by default, no clutter**: When Cover Image is switched off for a klass, the component simply doesn't render.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. **Open a generic element** that already has attachments or an analysis with images.
2. **Open the picker**: a button opens a modal listing **Candidate List** (from Attachments and Analyses) and **Selected** (what's currently shown).
3. **Select and order**: move images into Selected, then use the up/down arrows to set their display order.
4. **Close the modal** — the chosen images now page through at the top of the element, above its segments.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **A view over existing files.** Selections are stored per element, recording each image's source (attachment or analysis) and its id — not a copy of the file.
- **Fully opt-in.** The feature only appears where a Template Designer has switched it on for that element klass; other elements are unaffected.

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
