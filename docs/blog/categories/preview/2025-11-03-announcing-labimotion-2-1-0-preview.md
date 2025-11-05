---
layout: default
title: "Version 2.1.0 Public Preview"
date: 2025-11-05
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20251031
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

Scientific research requires clear traceability from materials to results. We extend the "Link Element" (aka "Drag Element") field type and it is able to accept hard-coded elements or generic elements. Our new **Element Linking** features enable:

- **Link Element to Element**: Associate elements - whether hard-coded elements (such as wellplates) or generic elements - with your generic elements.
- **Link Element to Dataset**: Similar to Element-to-Element linking, this allows associating elements with your datasets.

{: .note}
**Note for Designer**
We now unify the field type name to "Link Element", "Link Molecule", and "Link Sample" (it was "Drag Element", "Drag Molecule", and "Drag Sample").

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

Tables - such as measurement data - can now be exported in XLSX format.

- **Format**: XLSX
- **SMILES by default**: For chemical data (sample), SMILES is included by default
- **Image URL link**: For chemical data (sample or molecule), an image link is provided

This makes it easier to share data with collaborators or import it into various analysis tools.

(**Table Export Button** - Click to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Table Export](/assets/images/posts/2-1-0-preview/table_export_button.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/table_export_button.png){:target="_blank"}

(**Tabel Export File** - Click to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Table Export in XLSX](/assets/images/posts/2-1-0-preview/table_export_xlsx.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/table_export_xlsx.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### ✏️ Text Field with Auto-Link Support

The enhanced Text Field now supports automatic URL recognition, converting URL-like text into clickable links.

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

A new experimental feature, **Source Information**, is now available for Generic Datasets. It displays metadata provided by the system or extracted from uploaded files. This feature contains two sections and will become the default for all Generic Dataset templates.

- **General Description**: Common information such as date, time, creator, etc.
- ***Element* Details**: Re/Source element information such as re/source type (sample or reaction), re/source ID (sample ID or reaction ID), etc. The title of this section identify the source element itself, for example, if the source type is a sample, the title shows as "Sample details".

(**Generic Dataset Source Information** - Click to open in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Generic Dataset Source Information](/assets/images/posts/2-1-0-preview/dataset_source_information.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/dataset_source_information.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 📏 Supported Units

Additional unit options are now available - for example, Power, Pressure, and Volume (metric-based) units.
See the full list and discussion here:
[Supported Units for System Defined Field](https://github.com/LabIMotion/labimotion/wiki/Supported-Units-for-System-Defined-Field)

### more characters for element identifer

Support for more characters when naming an element.


[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 🎨 UX Improvements

Several enhancements have been introduced to improve the overall user experience.

- Color examples when configuring the layer header
- Resizable panels in the **Work Area** for a flexible workspace
- Display of overall version information
- One-click access to a full list (`Full List` button)
- Alphabetical sorting of active element types

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How to Participate in the Preview

1. 🖥️ **Visit the Test Instance:** [Link to Test Instance](https://labimotion-stage.ibcs.kit.edu/home)
2. 🔍 **Explore the New Features:** Try out the enhancements and see how they support your work.
3. ❤️ **Provide Feedback:** Please share your feedback in our discussion thread:
   [Link to Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/39).

We appreciate your participation and look forward to your feedback.

Thank you!

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
