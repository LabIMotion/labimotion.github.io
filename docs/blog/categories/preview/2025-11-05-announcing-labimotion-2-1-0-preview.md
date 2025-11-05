---
layout: default
title: "Version 2.1.0 Public Preview"
date: 2025-11-05
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20251105
categories: [Announcements, Preview]
has_toc: true
---

Chemotion LabIMotion 2.1.0 is now available for public preview!
{: .fs-7 .fw-500 }

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

Dear Chemotion LabIMotion users,

Welcome to the preview of Chemotion LabIMotion 2.1.0!

## What's New in v2.1.0?

### 🔗 Link Materials to Data: Element Linking

Scientific work requires clear traceability between materials and resulting data. The existing **“Link Element”** field type (formerly “Drag Element”) has been extended and now supports both hard-coded elements and generic elements.

The new **Element Linking** features include:

- **Link Element to Element**: Associate elements - such as hard-coded elements (e.g., wellplates) or generic elements - with other generic elements.
- **Link Element to Dataset**: Similar to Element-to-Element linking, this allows associating elements directly with datasets.

{: .note}
**Note for Designers**
Field type names have been unified to **"Link Element"**, **"Link Molecule"**, and **"Link Sample"** (previously "Drag Element", "Drag Molecule", and "Drag Sample").

(**Link Element to Element** - Click the video to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2-1-0-preview/link_element_to_element.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2-1-0-preview/link_element_to_element.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

(**Link Element to Dataset** - Click the video to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0%;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2-1-0-preview/link_element_to_dataset.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2-1-0-preview/link_element_to_dataset.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 📤 Export with Ease: Table Export

Tables - such as measurement data - can now be exported in **XLSX** format.

- **Format:** XLSX
- **SMILES by default:** For chemical data (samples), SMILES are included by default
- **Image URL links:** For chemical data (samples or molecules), an image link is provided

This makes it easier to share data with collaborators or import it into various analysis tools.

(**Table Export Button** - Click to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Table Export](/assets/images/posts/2-1-0-preview/table_export_button.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/table_export_button.png){:target="_blank"}

(**Table Export File** - Click to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Table Export in XLSX](/assets/images/posts/2-1-0-preview/table_export_xlsx.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/table_export_xlsx.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### ✏️ Text Field with Auto-Link Support

The enhanced Text Field now supports automatic URL recognition, converting URL-like text into clickable hyperlinks.

(Click the video to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2-1-0-preview/text_field_auto_link.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2-1-0-preview/text_field_auto_link.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 🧪 Generic Dataset Source Information (experimental)

A new experimental feature, **Source Information**, is now available for Generic Datasets. It displays metadata provided by the system or extracted from uploaded files. This feature contains two sections and is expected to become the default for all Generic Dataset templates.

- **General description**: Common information such as date, time, creator, etc.
- ***Element* details**: Source element information such as source type (sample or reaction), source ID (sample ID or reaction ID), etc. The section title reflects the corresponding source element, for example, "Sample details".

(**Generic Dataset Source Information** - Click to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Generic Dataset Source Information](/assets/images/posts/2-1-0-preview/dataset_source_information.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/dataset_source_information.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 📏 Supported Units

Additional unit options are now available - for example, Power, Pressure, and metric-based Volume units.

The complete list is available here:
[Supported Units for System Defined Field](https://github.com/LabIMotion/labimotion/wiki/Supported-Units-for-System-Defined-Field)

### 🔠 Extended Element Identifier Length

Element identifiers now support a longer character range, with the allowed length expanded to 3-10 characters

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 🎨 UX Improvements

Several improvements have been introduced to enhance the overall user experience:

- Color examples when configuring the layer header
- Resizable panels in the **Work Area**
- A summary of the version information
- One-click access to a complete list (`Full List` button)
- Alphabetical sorting of active element types

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How to Participate in the Preview

1. 🖥️ **Visit the Test Instance:**
   [Link to Test Instance](https://labimotion-stage.ibcs.kit.edu/home)

2. 🔍 **Explore the New Features:**
   Try out the enhancements and evaluate how they support your work.

3. ❤️ **Provide Feedback:**
   Please share your comments in our discussion thread:
   [Link to Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/39)

We appreciate your participation and look forward to your feedback.

Thank you!

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
