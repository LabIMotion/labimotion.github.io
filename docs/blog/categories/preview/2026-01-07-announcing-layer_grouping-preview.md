---
layout: default
title: "(New) Layer Grouping"
date: 2026-01-07
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260107
categories: [Announcements, Preview]
has_toc: true
---

(New) Layer Grouping
{: .fs-7 .fw-500 }

---

**Layer Grouping** is a major new feature that allows you to bundle multiple layers into a single logical unit. Instead of managing dozens of individual layers, you can now organize them into cohesive blocks and control their visibility with a single rule.

**The Benefits**

- For Designers (Efficiency)

  - **Unified Management**: Move, organize, and manage multiple layers as one.
  - **Bulk Visibility**: Set one restriction on a group to hide or show all its containing layers at once. No more repeating the same rule for every layer.

- For End-Users (Experience)

  - **Chapter-Based Navigation**: Information is organized into intuitive "chapters" rather than a flat, overwhelming list of layers.
  - **Improved Context**: Group headers provide clear context for why a set of layers is being displayed.
  - **Cleaner Interface**: Groups keep related data visually bundled, making the form easier to scan and understand.
  - **Smart Forms**: Irrelevant modules are hidden in bulk, so users only see the "story" that applies to their specific data entry.


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

Forms respond instantly to your input. When you pick a specific option (like a checkbox or dropdown), the system evaluates if a whole group should appear.

1. **Organization**: Sections are visually bundled into titled chapters.
2. **Context**: Group headers clearly label the purpose of the collection.
3. **Dynamics (Optional)**: If rules are set, entire collections appear/disappear based on your input.

*Note: Grouping is valuable for organization even if you don't use visibility rules!*

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

## How to Setup (For Designers)

Configuration is managed through the new **Group & Restrictions** button in the Template Designer.
If you have permission to edit form templates, you can configure which fields appear in the title by following these steps:

1. **Open Designer**: Click the **Group & Restrictions** button.
2. **Setup Groups**: Click **Assign to a group** on layers to bundle them together.
3. **Apply Bulk Rules**: Click the **Restriction** button on a **Group Header**.
4. **Choose Trigger**: Select the field and value that should reveal the group.
5. **Save**: Click **Save** and then **Release** your template changes.

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }


## Example Scenarios

### Scenario 1: Mixed Hybrid Layout (Visual Organization)
**Goal**: Organize a long form into logical chapters while keeping primary information immediately visible and individual.

*   **Group A**: "Facility Information" (Contains: Address, Contact, and GPS layers).
*   **Ungrouped Layer**: "Primary Status" (Kept outside for immediate visibility).
*   **Group B**: "Safety Logs" (Contains: Incident History and Safety Gear layers).
*   **Ungrouped Layer**: "Final Comments".

**User Experience**: The user sees a clear, structured flow where high-level categories (Facility Info, Safety Logs) act as containers, but the most critical individual layers (Primary Status) stay prominent and standalone.

### Scenario 2: Conditional Chapter Visibility (Power Logic)
**Goal**: Only show multiple "Security Audit" layers if the "Audit Required" toggle is ON.

*   **The Group Way**:
    1. Create a group called "Security Audit Block".
    2. Put 5 relevant layers into this group.
    3. Add **one** restriction to the "Security Audit Block" group: `Audit Required = true`.

**User Experience**: Instead of the form appearing cluttered with 5 empty layers, the whole "Security Audit" chapter appears instantly only when the user signifies that an audit is necessary.

---

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

## How to Participate in the Preview

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
