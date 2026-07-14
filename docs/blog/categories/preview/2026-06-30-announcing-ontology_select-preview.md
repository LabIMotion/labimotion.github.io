---
layout: default
title: "(New) Ontology Selection Field Type"
date: 2026-06-30
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260630
categories: [Preview]
has_toc: true
description: Pick a term from a controlled ontology tree instead of typing free text.
---

(New) Ontology Selection Field Type
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

The new **Ontology selection** field lets users choose a value from a controlled vocabulary — browsing a hierarchical term tree served by the [TIB Terminology Service](https://terminology.tib.eu/) — instead of typing free text. The chosen term's label is stored on the field, keeping your data human-readable and consistent across every element.

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

- **Controlled vocabulary**: Values come from an OBO Foundry ontology, not a static option list or free text — so terms stay authoritative and centrally maintained.
- **Tree browser**: Users explore the ontology with an expandable tree and a live definition panel, rather than guessing at the right wording.
- **Search as you type**: Filter the tree by label in real time, with matching branches auto-expanded.
- **Human-readable storage**: The term's **label** is what gets saved, so exported data reads naturally.
- **Restriction source**: Because the stored value is a single label, an ontology field can show or hide other fields depending on which term was picked.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Designers — adding an ontology field

1. Add a field and set its type to **Ontology selection**.
2. Set the field's **ontology root term** — the entry point of the tree the user will browse, given as an ontology id plus the term's IRI (for example `bao:class:http://purl.obolibrary.org/obo/BAO_0000103`). The root term and everything beneath it become selectable.
3. *(Optional)* Use the field as a **restriction source**. In the field restriction setup, pick the ontology field and choose the term that should trigger the restriction — the same tree browser is used to pick it. Other fields then react to whether the user's selection matches.

What persists in the template is the **root term** (the source), not a copy of the whole ontology — the tree is fetched live.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## For Users — picking a term

1. Click the field (or its **Term** button). A modal opens with the ontology tree on the left and a definition panel on the right.
2. **Browse or search.** Expand and collapse branches with the arrows, or type in the search box to filter the tree by label in real time. Hover a term to read its **definition** in the side panel.
3. **Select** a term by clicking it — the modal closes and the field shows the term's label.
4. **Clear** a selection with the **×** in the field.
5. **Refresh** — if terms seem missing or out of date, use the **Refresh** button in the modal to clear the locally cached tree and re-fetch it from the server.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **Terms come from a terminology service.** The tree is fetched from the TIB Terminology Service for the configured ontology, so the vocabulary is authoritative rather than copied into the template.
- **Lazy load, then cache.** The full tree under the root term loads on first open and is kept locally, so reopening the picker is instant. A partial or incomplete tree is rejected rather than cached — you never browse a half-loaded vocabulary.
- **The label is the value.** Selecting a term stores its label, so an ontology field behaves like any other select-style source — including for restrictions.
- **The tree follows the field.** When the field a restriction points at changes, the picker reloads the correct ontology tree instead of leaving a stale one on screen.

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
