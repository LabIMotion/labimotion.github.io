---
layout: default
title: "(New) System User Selection"
date: 2026-06-27
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260627
categories: [Announcements, Preview]
has_toc: true
description: Point a Select field at the host's real user directory instead of a fixed option list.
---

(New) System User Selection
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

A **System User Selection** field points an ordinary **Select** or **Select (Multiple)** field at the host application's user directory — Chemotion ELN users — instead of a fixed option list typed into the template. Users search for and pick real people, and only their **user ids** are stored. There is **no new field type** to learn: it is the same select field, simply configured to use the user list as its option source.

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

- **Real people as options**: The field offers actual host users instead of a hand-typed list — nothing to maintain when your team changes.
- **No new field type**: Reuses the existing **Select** / **Select (Multiple)** field; you just choose the user list as its option source.
- **Async search**: Type a few characters and the field searches the host's user directory, showing up to 5 matches.
- **Live names, stored ids**: Only ids are saved; names are looked up fresh, so a renamed user always shows their current name.
- **Resilient selections**: A user who no longer exists shows with extra `(depr.)` rather than silently vanishing.
- **Compact multi-select**: Up to 2 picks show as inline chips; the rest collapse into a `+N` popover.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Designers — binding a field to the user list

1. Add or edit a **Select** or **Select (Multiple)** field.
2. For its **option source**, choose **"System user list"** instead of typing options. You do **not** add any option entries.
3. That's it. The field now shows a friendly **"System user list"** instead of a static option list.

What persists in the template is only the **source choice** — there is no option list to maintain, and no user names are baked into the template.

{: .info }
> **Scope:** This applies to a **Select** / **Select (Multiple)** field placed in a **layer**. It is **not** available for a **Select** column inside a **Table** field — a table column's option source offers only static selection lists, not the system user list.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Users — picking users

- The field is an **async picker**. Start typing a name; after **3 or more characters** it searches the host's user list and shows up to **5 matches**. A muted hint under the field reminds you of the 3-character minimum; fewer characters does nothing.
- Pick **one** user (single-select) or **several** (multi-select).
- **Already-saved selections** show each user's **current** name when you open the element — names are looked up live, so a user who was renamed shows their new name.
- A user who **no longer exists** (e.g. deleted) shows with extra **`(depr.)`** so the selection stays visible rather than silently vanishing.
- **Multi-select:** up to **2** picks show as inline chips; any beyond that collapse into a **`+N`** button. Click it to review the rest and remove individual ones. When the field is **read-only**, you can still open the popover to view the hidden items but not remove them.
- **What's stored:** only the **user ids** — never names.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **A marker selects the source.** Choosing "System user list" tags the field with a special option-source value instead of an option list. When the renderer sees that marker, it mounts the async user picker in place of the normal static dropdown.
- **Live names, stored ids.** Only ids are saved. Names are always fetched fresh, so renames are reflected automatically and a selection never goes stale.
- **Fetch and cache.** Looked-up users are kept in a shared cache keyed by id that survives tab switches and remounts, so many user fields on one page don't repeat the same lookups.
- **Backfill on open.** When the element opens, any saved ids that aren't already cached are resolved so saved selections show real names immediately instead of placeholders.
- **Orphans don't disappear.** An id that resolves to nothing falls back to `(depr.)` rather than being dropped, keeping the selection intact.
- **Clear on source change.** If a Designer switches a field's option source, any previously stored selection is cleared, so ids from the old source can't leak into the new one.

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
