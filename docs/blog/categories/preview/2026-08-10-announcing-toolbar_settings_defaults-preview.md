---
layout: default
title: "(New) Toolbar Settings — Default Overview & Expand"
date: 2026-08-10
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260810
categories: [Preview]
version: 2.4.0-rc
has_toc: true
description: Your personal Toolbar Settings, under My LabIMotion, now genuinely control whether the overview map and layer panels start open when a form opens.
---

(New) Toolbar Settings — Default Overview & Expand
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
  version=page.version
%}

**Toolbar Settings** — your own, under **My LabIMotion** — let you decide how a detail form looks the moment it opens. Two of its three switches now work as intended: **Overview** and **Expand**. The page also got a search box and a visual refresh, so finding the row you want is quicker.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** All Users
>
> **Interface:** Chemotion ELN / top-right user menu → **My LabIMotion** → **Toolbar Settings**
{: .info }

- **Overview default**: turns the Overview map open or closed the moment a form opens. The button itself always stays available, so you can still open or close it yourself in the moment.
- **New Expand default**: turns every layer open on load, or just the first one (the previous, implicit behavior — now an explicit, working switch).
- **Arrange, alongside them**: a third switch on the same row shows or hides the Arrange button in the toolbar — unchanged from before, just now sitting next to the other two.
- **Same setting, two places**: change these from the Toolbar Settings page, or from the gear icon right on the form.
- **Find a row faster**: a live search box filters both the **Elements** and **Segments** cards by label, with a match-count badge (e.g. "1/4") and an empty-state message when nothing matches.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## What It Looks Like

This is the real **Toolbar Settings** page — one row per element or segment, three switches each:

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 .text-center }

[![Toolbar Settings page under My LabIMotion, listing Elements and Segments each with Overview, Expand and Arrange switches](/assets/images/posts/2026-08-10-toolbar-settings-preview/toolbar-settings.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-08-10-toolbar-settings-preview/toolbar-settings.png){:target="_blank"}

Hovering the **?** next to each column name gives the exact rule: **Overview** — *"Show the Overview map when the form opens."* **Expand** — *"Expand all layers when the form opens (off: only the first layer)."* **Arrange** — *"Show the Arrange button in the toolbar."*
{: .fs-2 .mb-0 .text-center }

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. Click your name in the top-right corner → **My LabIMotion** → **Toolbar Settings**.
2. Use the search box to jump straight to the element or segment you use most — e.g. typing "sample" narrows both cards down to their matches, with a live count.
3. Turn **Overview** off if you don't want the map open every time you open a form; turn **Expand** on if you'd rather every layer open right away.
4. Next time you open a matching form, it reflects your defaults — and the Overview, Expand and Arrange controls on the form itself still work normally to change things for that session.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- These are **personal, per-element or per-segment defaults** — set on your own account under **My LabIMotion**, they don't change what your colleagues see.
- The Overview, Expand and Arrange controls on the form keep working as manual, in-session toggles no matter what your defaults are set to.

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
