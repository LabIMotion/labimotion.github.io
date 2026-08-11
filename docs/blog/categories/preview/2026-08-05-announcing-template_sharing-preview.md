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
version: 2.4.0-rc
has_toc: true
description: Every Designer template now has an owner, who decides who else may view, edit, or take it over.
---

(New) Template Ownership & Sharing
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
  version=page.version
%}

Until now, any designer of a family — elements, segments or datasets — could edit or delete **any** template in it, with nothing recording whose work it was. From this release, each template has an **owner**, and colleagues work on it by invitation or by asking.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Designers
>
> **Interface:** Chemotion ELN / Generic Elements, Segments and Datasets Designer
{: .info }

- **Every template gets an owner**: one named designer per template, shown in a new **Owner** column in the Designer grid.
- **Share it deliberately**: the owner grants colleagues **Viewer** (look, don't touch) or **Editor** (draft, can't release) access from a new **+Share** dialog, or hands the template over entirely with **Transfer ownership**.
- **Ask when you need it**: on a template you can't open, a **Request access** button lets you ask the owner directly; they see it waiting in their Share dialog and in a new inbox.
- **Three tabs to browse by**: **Owned by me**, **Shared with me**, and **All** — so you can still find and request access to any template in the instance.
- **Delete moved to a Danger zone**: deleting a template is now owner-only, behind a confirmation checkbox, separate from everyday actions.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## What It Looks Like

The Designer grid gains one new column — **Owner** — plus the sharing icons in **Access**. Here's the real **Generic Elements Designer**, on the **All** tab: some templates are owned by Paggy Huang, one by Nicole Jung, the rest still by the system's **ELN Admin** account:

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 .text-center }

[![Generic Elements Designer grid, All tab, showing the Owner column and per-row Access icons](/assets/images/posts/2026-08-05-template-sharing-preview/designer-grid-owner-column.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-08-05-template-sharing-preview/designer-grid-owner-column.png){:target="_blank"}

The green check or red no-entry icon under **Access** is the **Active** toggle — whether the template is switched on for the instance — and has nothing to do with who can open it. The **person-plus** button next to it, **Share this template**, is enabled only for the owner; everyone else sees it greyed out. A row you don't have access to also carries a **paper-plane** button — **Request access**. Click it, and it turns into a clock with a tooltip confirming the request is waiting.

Opening **Share this template** on "Device Description" (owned by Nicole Jung) shows Paggy's request still pending:

[![Share dialog for Device Description, showing Paggy Huang's access request waiting for a decision](/assets/images/posts/2026-08-05-template-sharing-preview/share-dialog-pending-request.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-08-05-template-sharing-preview/share-dialog-pending-request.png){:target="_blank"}

Nicole picks **Editor** from the **Grant…** dropdown next to the request. The request row is replaced by a **People with access** row, with a level dropdown, a **transfer-ownership** button (⇄), and a **remove** button (bin):

[![Same Share dialog after granting Editor access: Paggy Huang now listed under People with access, with level dropdown, transfer and remove buttons](/assets/images/posts/2026-08-05-template-sharing-preview/share-dialog-granted-access.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-08-05-template-sharing-preview/share-dialog-granted-access.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. On the **All** tab, Paggy (CHI) finds "Device Description", owned by Nicole (NJ), and clicks **Request access** — the button turns into a clock: *"Nicole Jung has your request. Not granted yet — it waits in their Share dialog. You can ask again."*
2. Nicole opens **Generic Elements Designer**; the row's **Share** button now carries a waiting-count badge. Opening it shows Paggy's request under **Access requests**.
3. Nicole picks **Editor** from the **Grant…** dropdown. Paggy now appears under **People with access**, with a level dropdown, a **transfer-ownership** button, and a **remove** button.
4. As an **Editor**, Paggy can draft and save; only Nicole, the owner, can release, activate/deactivate, delete, or manage sharing further — unless she uses the transfer button to hand ownership to Paggy outright.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **A coordination feature, not a new lock.** Every designer of a family was already authorized to touch its templates; this adds a record of who's responsible for each one, and a reason to ask first.

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
