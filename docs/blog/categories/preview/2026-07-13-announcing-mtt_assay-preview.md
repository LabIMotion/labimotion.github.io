---
layout: default
title: "(New) MTT Assay"
date: 2026-07-13
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260713
categories: [Announcements, Preview]
has_toc: true
description: Turn wellplate readings into dose-response curves and IC50 values, then attach the results back to your samples.
---

(New) MTT Assay
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

The new **MTT Assay** workflow takes cell-viability wellplate data through a full **dose-response analysis** and brings the results back into the ELN. From a Generic Element's **Wellplates** tab you submit selected wellplates for processing, track each request's status, review the computed **IC50** and **dose-response curves**, and then send the analyses you trust back to the corresponding **samples** as measurements.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Researchers, Template Designers
>
> **Interface:** Chemotion ELN / Generic Element – Wellplates & Measurements tabs
{: .info }

- **Wellplate-to-analysis pipeline**: Select one or more wellplates on a Generic Element and submit them for dose-response processing in a single action.
- **Request tracking**: A **Request Status** table shows every submission — its state (*initial*, *processing*, *completed*, *error*), created/expiry times, active/expired/revoked status, and any service message — with one-click **Refresh** and **Delete**.
- **Dose-response results**: For each analysed molecule you get a compact **box-plot preview** of its dose-response curve plus the key metrics: **IC50** (relative), its **lower** and **upper** bounds, and **pIC50**, with an **OK / Problems** status flag.
- **Full analysis details**: Open any result to see the enlarged dose-response visualization, the complete metrics table (Hill coefficient, RSE, p-value, asymptotes, problems), and the underlying input rows (concentration, values, well / sample / wellplate IDs).
- **Send results to samples**: Select the analyses you want and push them, in bulk, to their **samples** as measurements — so the dose-response outcome lives alongside the substance it describes.
- **Results in the Measurements tab**: Each sample's **Measurements** tab lists its MTT analyses grouped by assay type, with IC50 / pIC50 metrics, a link back to the originating Generic Element, and per-row delete.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Users — running an analysis

> **Audience:** Researchers
>
> **Interface:** Generic Element – Wellplates tab
{: .info }

1. **Open the Generic Element** that holds your assay and switch to the **Wellplates** tab.
2. **Attach wellplates**: Drop a wellplate onto the drop area (or use those already linked) so its plate data is available for analysis.
3. **Select wellplates**: Tick the wellplates you want to include in this run.
4. **Submit**: Click to process the selection. A new entry appears in the **Request Status** table while the dose-response service computes the curves.
5. **Track progress**: Use **Refresh** to update the state until the request reads **completed**. If something goes wrong, the row turns **error** and shows the service's message.

[![Request Status table showing submitted MTT analysis requests and their states](/assets/images/posts/2026-07-13-mtt-assay-preview/request-status.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-07-13-mtt-assay-preview/request-status.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Reviewing results

Once a request is **completed**, expand its **Outputs** to see the results table. Each row is one analysed molecule:

| Column | Meaning |
| :--- | :--- |
| **Molecule** | Name of the analysed sample. |
| **Dose Response** | A thumbnail of the fitted dose-response curve — click to open the full view. |
| **IC50 / Lower / Upper** | The relative IC50 estimate and its confidence bounds. |
| **pIC50** | The negative log of the IC50. |
| **Status** | **OK**, or a **Problems** badge when the fit flagged an issue. |

[![Results table listing analysed molecules with IC50, pIC50 and dose-response thumbnails](/assets/images/posts/2026-07-13-mtt-assay-preview/results-table.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-07-13-mtt-assay-preview/results-table.png){:target="_blank"}

Click any result (or the **details** action) to open the **Analysis Details** view, which shows:

- **Dose-Response Visualization** — the full-size curve for the selected molecule.
- **Results** — the complete metrics table: IC50 (relative), lower/upper bounds, pIC50, Hill coefficient, RSE, p-value, asymptotes, and problems.
- **Input Data Summary** — the raw rows behind the fit: name, concentration, measured values, and well / sample / wellplate identifiers.

[![Analysis Details modal with the full dose-response curve, metrics table and input data summary](/assets/images/posts/2026-07-13-mtt-assay-preview/analysis-details.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-07-13-mtt-assay-preview/analysis-details.png){:target="_blank"}

You can **select** individual results (or **select all**) with the checkboxes, and **delete** any analysis you no longer need.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Sending results back to samples

The point of an assay is to describe a substance — so the results belong with the sample.

1. **Select** the analyses you trust in the results table.
2. **Send to samples**: Push the selection in one action. Each analysis becomes a **measurement** on its matching sample, tagged with the assay's label so you know where it came from.
3. **Confirmation**: A notification reports how many measurements were created (and flags any that failed).
4. **View on the sample**: Open the sample's **Measurements** tab. MTT analyses are grouped by assay type and list the same IC50 / pIC50 metrics, a **status** flag, a link to **open the originating Generic Element**, and a delete action per row.

[![Sample Measurements tab showing MTT analysis results grouped by assay type](/assets/images/posts/2026-07-13-mtt-assay-preview/measurements-tab.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2026-07-13-mtt-assay-preview/measurements-tab.png){:target="_blank"}

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **Wellplate readings become dose-response fits.** Submitted plate data is sent to a dose-response service that fits a curve per molecule and returns IC50, pIC50, confidence bounds, and goodness-of-fit metrics.
- **Requests are first-class and traceable.** Every submission is stored as a request tied to its Generic Element, with its own lifecycle (initial → processing → completed / error), expiry, and message — so nothing is a black box.
- **Results are stored as measurements.** Sending an analysis to a sample writes the metrics into the sample's measurement records, keyed back to the originating element, so exports and the Measurements tab all see the real numbers and the provenance link.

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
