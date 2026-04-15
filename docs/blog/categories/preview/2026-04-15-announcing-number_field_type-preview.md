---
layout: default
title: "(New) Number Field Type"
date: 2026-04-15
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260415
categories: [Announcements, Preview]
has_toc: true
description: Enhanced numeric input with decimal precision, min/max constraints, and scientific notation.
---

(New) Number Field Type
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

The new `number` field type is designed to replace the limited `integer` type, providing advanced configuration options for numeric data in LabIMotion templates.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers, Researchers
>
> **Interface:** LabIMotion Hub / ELN Template Designer
{: .info }

- **Decimal Precision**: Configure the maximum number of decimal places for each field.
- **Range Constraints**: Set optional minimum and maximum values to ensure data integrity.
- **Scientific Notation**: Full support for scientific notation (e.g., `1e10`, `1.2e-3`) for handling extreme values.
- **Smart Validation**: User input is automatically rounded and clamped based on the designer's constraints.
- **Visual Hints**: Users see active constraints (precision, min, max) directly below the input field for better guidance.
- **Flexible Separators**: Accepts both `.` and `,` as decimal separators for international compatibility.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Designer Configuration

The `number` field in the template designer now includes intelligent handling for configuration settings:

- **Automatic Cleanup**: If you enter invalid settings for decimal places (like negative numbers or fractions), the system automatically corrects them to the nearest valid integer and provides a helpful warning.
- **Precision Alignment**: If you set a minimum or maximum value that has more decimal places than the field allows, the system will automatically round those constraints to match the field's precision.
- **Seamless Reset**: Clearing the decimal setting will silently reset it to `0`, maintaining a stable configuration.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Support for Researchers

When researchers fill out an element, the `number` field provides real-time guidance and automatic correction:
- **Intelligent Clamping**: The system automatically adjusts input to stay within the designer's defined boundaries. For example, if a field is set with 1 decimal and a maximum of 10.0, entering "10.1" will automatically be corrected to "10.0".
- **Visual Hints**: A muted hint appears below the field showing the required precision and any active limits (e.g., `(dec: 1, min: 1, max: 10)`).
- **On-the-fly Validation**: Input is validated as you move between fields, ensuring data remains accurate and consistent.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Automatic Migration

Existing `integer` fields are automatically migrated to the `number` type with `decimals: 0` when the template is loaded in the designer, ensuring a seamless transition without data loss.

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
> Share your comments or report any issues in our [GitHub Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/67).

We appreciate your help in testing these new features!

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
