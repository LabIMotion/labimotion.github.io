---
layout: default
title: "(Experimental) Overview Map"
date: 2026-03-25
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260325
categories: [Announcements, Preview]
has_toc: true
description: Real-time Progress and Precision Navigation at Your Fingertips.
---

(Experimental) Overview Map
{: .fs-7 .fw-500 }

Real-time Progress and Precision Navigation at Your Fingertips.
{: .page-subtitle }

The **Overview Map** feature provides a visual dashboard at the top of your form to track data entry progress and streamline navigation. Instead of scrolling through long, multi-layered forms, you can see a high-level summary of your completion status and jump directly to any section with a single click.


---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## How It Works

> **Audience:** Users
>
> **Interface:** Chemotion ELN – MyDB view
{: .info }

The **Overview Map** acts as a "mission control" for your data entry process. Each section of your form is represented as a card that monitors your activity in real-time [1]. This is especially useful for intricate forms where multiple sections and sub-tasks must be tracked simultaneously.

 [![Overview Map](/assets/images/posts/2026-03-25-overview-map-preview/1.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-03-25-overview-map-preview/1.png){:target="_blank"}


**Primary Benefits:**
*  **Progress Visibility**: Instantly see which sections are complete via **color-coded bars** and **completion percentages**.
*  **Rapid Navigation**: Use the **blue "↓" icons** on map cards to instantly bypass long forms.
*  **Precision Focus**: Target sections are briefly **highlighted in yellow** upon arrival so you can immediately find your place.
*  **Layered Tracking**: Expand grouped sections (like "Reaction Info") within the map to monitor the progress of specific sub-tasks across multiple layers.

[![Overview Map](/assets/images/posts/2026-03-25-overview-map-preview/2.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-03-25-overview-map-preview/2.png){:target="_blank"}

**Logic Steps:**
The system tracks input fields to provide live feedback as you work.

1.  **Input Detection**: The user enters data into form fields, such as "Time," "Pressure," or "Observation".

2.  **Progress Calculation**: The system automatically calculates the completion percentage for that specific section.

3.  **Map Update**: The corresponding card in the Overview Map updates its color bar and percentage instantly, such as moving from **17% to 67%**.

4.  **Navigation Trigger**: The user clicks the blue arrow icon on a map card.

5.  **Auto-Scroll & Highlight**: The page automatically scrolls to the section and highlights it in yellow.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

Imagine you are filling out a "New Catalysis - Characterization" report. The Overview Map helps you track multiple sections simultaneously.

| Action | Resulting Map/Form State | Screenshot Reference |
| ------ | ------ | ------ |
| **Initial State** | "Device and setting" shows **17% completion** with a red progress bar. | [![Initial State](/assets/images/posts/2026-03-25-overview-map-preview/s1.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-03-25-overview-map-preview/s1.png){:target="_blank"} |
| **Enter Time, Pressure, and Observation** | Completion percentage jumps to **67%** in real-time. | Data entered |
| **Map Updates Instantly** | The bar turns orange and shows **67% completion**. | [![Map Updates Instantly](/assets/images/posts/2026-03-25-overview-map-preview/s2.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-03-25-overview-map-preview/s2.png){:target="_blank"} |

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

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
