---
layout: default
title: "(New) Template Ownership & Sharing"
date: 2026-08-05
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260805
categories: [Preview]
has_toc: true
description: Every Designer template now has an owner, who decides who else may view, edit, or take it over.
---

(New) Template Ownership & Sharing
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

Until now, any designer of a family — elements, segments or datasets — could edit or delete **any** template in it, with nothing recording whose work it was. From this release, each template has an **owner**, and colleagues work on it by invitation or by asking.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers
>
> **Interface:** Chemotion ELN / Element, Segment and Dataset Designer
{: .info }

- **Every template gets an owner**: one named designer per template, shown in a new **Owner** column in the Designer grid.
- **Share it deliberately**: the owner grants colleagues **Viewer** (look, don't touch) or **Editor** (draft, can't release) access from a new **+Share** dialog, or hands the template over entirely with **Transfer ownership**.
- **Ask when you need it**: on a template you can't open, a **Request access** button lets you ask the owner directly; they see it waiting in their Share dialog and in a new inbox.
- **Three tabs to browse by**: **Owned by me**, **Shared with me**, and **All** — so you can still find and request access to any template in the instance.
- **Delete moved to a Danger zone**: deleting a template is now owner-only, behind a confirmation checkbox, separate from everyday actions.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. On the **All** tab, find a colleague's template you'd like to help with.
2. Click **Request access** — your colleague sees a waiting request on their **+Share** button and in their inbox.
3. They grant you **Viewer** or **Editor** from the Share dialog; you're notified, and the template moves to your **Shared with me** tab.
4. As an **Editor** you can draft and save; only the owner can release, activate/deactivate, delete, or manage sharing.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **A coordination feature, not a new lock.** Every designer of a family was already authorized to touch its templates; this adds a record of who's responsible for each one, and a reason to ask first.
- **Nothing is stranded.** Templates with no recorded owner keep working exactly as before, open to every designer of that family.

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
