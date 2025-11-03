---
layout: default
title: "Version 2.1.0 Public Preview"
date: 2025-10-31
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

Welcome to the preview for Chemotion LabIMotion 2.1.0!

## What's New in v2.1.0?


### 🔗 Link Materials to Data: Element Linking

Scientific research requires clear traceability from materials to results. Our new **Element Linking** capabilities enable:

- **Link Element to Element**: Associate elements, no matter it is a hard-code element (e.g. wellplate) or a generic element, with your generic elements
- **Link Element to Dataset**: Similar to the `Link Element to Element`, you can associate elements to your dataset

(**Link Element to Element** Click video to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2-1-0-preview/link_element_to_element.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2-1-0-preview/link_element_to_element.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

(**Link Element to Dataset** Click video to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2-1-0-preview/link_element_to_dataset.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2-1-0-preview/link_element_to_dataset.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### 📤 Export with Ease: Table Export

Data with the table, e.g. measurement data, can be exported in a XLSX format.

- **Format**: Export to XLSX
- **SMILES as default**: For chemical data(sample), export includes SMILES format by default
- **Image url link**: For chemical data(sample or molecule), an image link is provided

Perfect for sharing data with collaborators or importing into other analysis tools.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Table Export](/assets/images/posts/2-1-0-preview/table_export.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/table_export.png){:target="_blank"}

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Table Export in XLSX](/assets/images/posts/2-1-0-preview/table_export_xlsx.png){: .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2-1-0-preview/table_export_xlsx.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### Text Field with Auto-Link Support

The enhanced Text Field supports automatic URL detection, automatically converts URL-like text into clickable links.

(Click video to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: start; margin-top: 0;">
  <video width="75%" controls autoplay loop muted onclick="window.open('/assets/images/posts/2-1-0-preview/text_field_auto_link.mp4', '_blank')" style="cursor: pointer;">
    <source src="/assets/images/posts/2-1-0-preview/text_field_auto_link.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### Generic Dataset Source Information (Experimental)

We have an experimental feature, `Source Information`, on Generice Dataset which display the data from the system or extracted from the files. It includes two parts - the "General Description" and "Element Details" for you. The `Source Information` will be the default for all Generic Dataset templates.

- **General Description**: It includes the common source information, e.g. date, time, creator...etc.
- **Element Details**: It includes the source element information, e.g. resource type (sample or reaction), resource id (sample id or reaction id)...etc.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### Supported Units

More unit options are provided, e.g. Power, Pressure and Volumes (Metric-based). See the full list and discussions at [Supported Units for System Defined Field](https://github.com/LabIMotion/labimotion/wiki/Supported-Units-for-System-Defined-Field)

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

### UX improvements

Several enhancements are intorudced in this version to gain better user experiences.

- Allow more characters for naming an element.
- Given the color examples when setting up the layer header.
- A resizable panels on the `Work Area` let you adjust your workspace.
- An overall version information.
- One click to display a full list (`Full List` button).
- List the active element type in alphabet order.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How to Participate in the Preview

1. 🖥️ **Visit the Test Instance:** [Link to Test Instance](https://labimotion-stage.ibcs.kit.edu/home)
2. 🔍 **Explore the New Features:** Dive into the new functionalities and see how they enhance your workflow.
3. ❤️ **Provide Feedback:** For the feedback of this preview, please share your thoughts and observations in our discussion thread [Link to Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/39).

We appreciate your participation and look forward to your feedback.

Thank you!

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
