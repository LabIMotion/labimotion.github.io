---
layout: default
title: "(New) Dynamic Layer Display Names"
date: 2026-01-13
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260113
categories: [Announcements, Preview]
has_toc: true
---

(New) Dynamic Layer Display Names
{: .fs-7 .fw-500 }

---

The **Dynamic Layer Display Names** feature makes it easier to manage and identify information by automatically updating a layer's title based on the data you enter. Instead of seeing generic titles like "Sample Information" repeated multiple times, you will see specific details like "Sample Information - Liquid" right in the header.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

## How It Works (For Users)

<br>

*For Users: e.g. in Chemotion ELN MyDB view*

Instead of navigating through multiple layers with the same generic layer name, this feature automatically builds a descriptive title as you work. This allows you to identify specific records (like a specific batch or detector type) without having to expand every layer.

**Primary Benefits:**
- **Navigation**: Instantly find the right layer in long forms.
- **Clarity**: High-level summary of the layer's content is always visible.
- **Accuracy**: Titles update in real-time as you modify data.

**Logic Steps:**

Layer titles update automatically as data is entered.

1. **Detect Change**: Form data is updated by the user.
2. **Field Check**: System checks if the field is configured to be part of the title.
3. **Visibility Check**: Hidden fields are ignored to prevent confusion.
4. **Empty Check**: If the field is empty or blank, it is skipped.
5. **Update**: Valid values are joined and appended to the section header.

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

## How to Setup (For Designers)

If you have permission to edit form templates, you can configure which fields appear in the title by following these steps:

**Configuration Steps:**
1. **Designer**: Access the Template Designer.
2. **Edit Layer**: Click the Pencil icon on the desired layer.
3. **Config Area**: Scroll to the "Advanced Display Name Setting".
4. **Select Fields**: Add desired fields to the active list.
5. **Finalize**: Click "Update" and then save/release your template changes.

**Key Points:**
- **Eligible Fields**: Only Dropdowns (Select) and Text fields can be used in titles.
- **Smart Logic**: Hidden or empty fields are automatically omitted.
- **Real-time**: Titles update instantly during form entry.

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

## Example Scenario

Imagine a "Safety Protocol" layer that is configured to show the **Hazard Level** and **Equipment Used**.

| Action | Resulting Layer Display Name |
| :--- | :--- |
| **Initial State** | Safety Protocol |
| **Select "High" Level** | Safety Protocol - High |
| **Type "Respirator" in Equipment** | Safety Protocol - High - Respirator |
| **Clear the Hazard Level** | Safety Protocol - Respirator |

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

## 🚀 How to Participate in the Preview

Follow these steps to explore the new features and share your insight:

{: .note }
> #### 1. 🖥️ Visit the Staging Instance
> Access the preview environment at: [labimotion-stage.ibcs.kit.edu](https://labimotion-stage.ibcs.kit.edu/home)
>
> #### 2. 🔍 Explore and Test
> Try out the enhancements — see how they fit your workflow.
>
> #### 3. ❤️ Your Feedback Matters
> Share your comments or report any issues in our [GitHub Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/67).

We appreciate your help in testing these new features!

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
