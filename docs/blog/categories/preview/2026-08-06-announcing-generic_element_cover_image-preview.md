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
version: 2.4.0-rc
has_toc: true
description: Give a generic element a cover image built from its own attachments and analyses, shown right above its tabs.
---

(New) Cover Image for Generic Elements
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
  version=page.version
%}

Generic elements can now show a **cover image** — a fixed-size strip of pictures rendered above the element's tabs, built from images you already have on the element. No separate upload: you pick from its existing **Attachments** and **Analyses**. A Designer switches it on for the element first.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## How It Works

> **Audience:** Users
>
> **Interface:** Chemotion ELN – Generic Element detail view
{: .info }

Where an element has Cover Image switched on, its page shows a fixed-size image block above its tabs, paging through whichever images you've picked for that element.

**Primary Benefits:**
- **Recognize at a glance**: Identify an element by sight before opening any tab or attachment.
- **Nothing new to upload**: Every image comes from what's already on the element — its **Attachments** and its **Analyses**.
- **Your pick, your order**: Choose which images show and in what order; anything not picked simply isn't shown.

**Using It:**
1. **Open the picker** on the element page, from its cover image area.
2. **Choose images** from a candidate list drawn from the element's Attachments and Analyses.
3. **Order them** — the order you choose is the order they page through in.
4. **Close it** — the strip above the tabs now shows your selection.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How to Setup

> **Audience:** Designers
>
> **Interface:** Generic Elements Designer → Template settings
{: .info }

Cover Image is opt-in per element, set from the same **Template settings** panel as the other layer-header controls — not from the Segment or Dataset Designer.

**Configuration Steps:**
1. From the top-right user menu, open the **Generic Designer** → **Generic Elements Designer**.
2. On the element's row, click the gear icon (**Template settings**) in the **Template** column.
3. Under **On the element page**, switch **Cover image** on.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 .text-center }

[![Template settings modal for the Viability element, showing the Cover image toggle under \"On the element page\"](/assets/images/posts/2026-08-06-cover-image-preview/template-settings-cover-image.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-08-06-cover-image-preview/template-settings-cover-image.png){:target="_blank"}

**Key Points:**
- **One switch among several**: Cover image sits under "On the element page", alongside the existing "On each layer header" controls (Record time, Add reaction, Add/remove layer) — each element is configured independently.
- **Immediate, not versioned**: the panel warns that the change *"applies to all versions of this template and takes effect immediately."*
- **Hiding doesn't delete data**: switching it off hides the block; any images already selected on elements aren't lost.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. A **Designer** opens **Generic Elements Designer**, clicks the gear icon on the **Viability** row, and switches **Cover image** on.
2. A **User** opens a Viability element that already has attachments or an analysis with images.
3. They open the cover image picker and pick a couple of images to show.
4. The chosen images now page through in a strip above the element's tabs — for every Viability element, until a Designer switches it off again.

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
