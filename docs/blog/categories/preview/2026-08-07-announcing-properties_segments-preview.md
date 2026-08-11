---
layout: default
title: "(New) Properties Segments"
date: 2026-08-07
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20260807
categories: [Preview]
version: 2.4.0-rc
has_toc: true
description: Embed a segment into an element's Properties tab (Scheme tab for reactions) instead of giving it a tab of its own, and optionally scope it to one element-type variant.
---

(New) Properties Segments
{: .fs-7 .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
  version=page.version
%}

Segments used to always get **their own tab**, on every element of their type. Now a segment can instead **embed inside the Properties tab** — or the **Scheme** tab, for reactions specifically — and optionally apply to only **one type variant** of that element.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Key Features

> **Audience:** Template Designers, Researchers
>
> **Interface:** Chemotion ELN / Segment Designer, Sample, Reaction and other element pages
{: .info }

- **Embed instead of a new tab**: a segment can render inside the **Properties** tab (Sample, Screen, Wellplate, …) or the **Scheme** tab (Reaction), stacked with a heading, instead of getting its own tab.
- **Narrow to a type variant**: an embedded segment can be scoped to one variant — **Micromolecule**/**Mixture** for samples, **Standard**/**Interaction** for reactions — or left on "all types".
- **Live filtering**: switch an element's type and matching embedded segments appear or disappear immediately — no reload.
- **Data isn't lost**: a segment that no longer matches the current variant is **hidden, not deleted** — its data comes back as soon as the variant matches again.
- **Generic elements unaffected**: generic element segments keep their own tab only; embedding and variants are for built-in elements.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Where Does a Segment End Up?

Every segment picks where it renders, and optionally which element-type variant it applies to:

<div style="display: flex; justify-content: center; margin: 1.5rem 0 0.5rem;">
<svg viewBox="0 0 740 350" role="img" aria-label="Flow showing where a segment can render, and the optional type-variant filter" style="display:block; max-width:100%; height:auto; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;">
  <defs>
    <marker id="seg-ah" viewBox="0 0 10 8" refX="9" refY="4" markerWidth="9" markerHeight="7" orient="auto">
      <path d="M0,0 L10,4 L0,8 z" fill="#8a8a8e"/>
    </marker>
    <marker id="seg-ahA" viewBox="0 0 10 8" refX="9" refY="4" markerWidth="9" markerHeight="7" orient="auto">
      <path d="M0,0 L10,4 L0,8 z" fill="#0071e3"/>
    </marker>
  </defs>

  <rect x="330" y="14" width="220" height="44" rx="22" fill="#fafafc" stroke="#d2d2d7" stroke-width="1.3"/>
  <text x="440" y="41" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">Assign segment to an element</text>
  <path d="M440,58 L440,86" stroke="#8a8a8e" stroke-width="1.4" fill="none" marker-end="url(#seg-ah)"/>

  <polygon points="440,88 574,132 440,176 306,132" fill="#eaf4ff" stroke="#0071e3" stroke-width="1.3"/>
  <text x="440" y="128" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">Segment Tab</text>
  <text x="440" y="145" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">setting</text>

  <path d="M306,132 L188,132" stroke="#8a8a8e" stroke-width="1.4" fill="none" marker-end="url(#seg-ah)"/>
  <text x="246" y="123" text-anchor="middle" fill="#6e6e73" font-size="12">New (own tab)</text>
  <rect x="24" y="104" width="164" height="56" rx="8" fill="#eef8f0" stroke="#2fa84f" stroke-width="1.3"/>
  <text x="106" y="128" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">Own tab</text>
  <text x="106" y="146" text-anchor="middle" fill="#6e6e73" font-size="12">applies to all variants</text>

  <path d="M400,165 L306,234" stroke="#0071e3" stroke-width="1.6" fill="none" marker-end="url(#seg-ahA)"/>
  <text x="308" y="192" text-anchor="middle" fill="#6e6e73" font-size="12">Properties tab</text>
  <rect x="176" y="234" width="230" height="52" rx="8" fill="#eef8f0" stroke="#2fa84f" stroke-width="1.3"/>
  <text x="291" y="256" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">Embedded in Properties tab</text>
  <text x="291" y="273" text-anchor="middle" fill="#6e6e73" font-size="12">Sample, Screen, Wellplate, …</text>

  <path d="M480,165 L576,234" stroke="#0071e3" stroke-width="1.6" fill="none" marker-end="url(#seg-ahA)"/>
  <text x="580" y="192" text-anchor="middle" fill="#6e6e73" font-size="12">Scheme tab (Reaction)</text>
  <rect x="470" y="234" width="230" height="52" rx="8" fill="#eef8f0" stroke="#2fa84f" stroke-width="1.3"/>
  <text x="585" y="256" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">Embedded in Scheme tab</text>
  <text x="585" y="273" text-anchor="middle" fill="#6e6e73" font-size="12">reactions only</text>

  <path d="M291,286 L400,318" stroke="#8a8a8e" stroke-width="1.4" fill="none" marker-end="url(#seg-ah)"/>
  <path d="M585,286 L480,318" stroke="#8a8a8e" stroke-width="1.4" fill="none" marker-end="url(#seg-ah)"/>
  <rect x="290" y="306" width="300" height="40" rx="8" fill="#fafafc" stroke="#d2d2d7" stroke-width="1.3"/>
  <text x="440" y="325" text-anchor="middle" fill="#1d1d1f" font-size="13" font-weight="600">Optional: narrow to one type variant</text>
  <text x="440" y="340" text-anchor="middle" fill="#6e6e73" font-size="11.5">Micromolecule/Mixture · Standard/Interaction</text>
</svg>
</div>

Green boxes are where you end up; blue diamonds are choices you make in the Designer.
{: .fs-2 .mb-0 .text-center }

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Setting It Up in the Designer

Both new controls live in the same **Segment Attributes** dialog you fill in when creating a segment:

<div style="display: flex; justify-content: center; margin: 1.5rem 0 0.5rem;">
<svg viewBox="0 0 500 360" role="img" aria-label="Simulated Segment Attributes dialog with Segment Tab set to Scheme tab and Reaction Type set to Interaction" style="display:block; max-width:100%; height:auto; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;">
  <rect x="20" y="10" width="460" height="340" rx="10" fill="#fafafc" stroke="#d2d2d7" stroke-width="1.3"/>
  <rect x="20" y="10" width="460" height="42" rx="10" fill="#f5f5f7"/>
  <rect x="20" y="32" width="460" height="20" fill="#f5f5f7"/>
  <text x="40" y="37" fill="#1d1d1f" font-size="14" font-weight="600">Segment Attributes</text>
  <text x="462" y="37" text-anchor="end" fill="#6e6e73" font-size="13">✕</text>

  <rect x="32" y="70" width="436" height="34" rx="6" fill="none" stroke="#d2d2d7" stroke-width="1.3"/>
  <text x="44" y="91" fill="#6e6e73" font-size="12">Segment Label</text>
  <text x="210" y="91" fill="#1d1d1f" font-size="12" font-family="ui-monospace, Consolas, monospace">Purification Details</text>

  <rect x="32" y="112" width="436" height="34" rx="6" fill="none" stroke="#d2d2d7" stroke-width="1.3"/>
  <text x="44" y="133" fill="#6e6e73" font-size="12">Description</text>
  <text x="210" y="133" fill="#1d1d1f" font-size="12" font-family="ui-monospace, Consolas, monospace">post-run purification data</text>

  <rect x="32" y="154" width="436" height="34" rx="6" fill="none" stroke="#d2d2d7" stroke-width="1.3"/>
  <text x="44" y="175" fill="#6e6e73" font-size="12">Assign to Element</text>
  <text x="210" y="175" fill="#1d1d1f" font-size="12" font-family="ui-monospace, Consolas, monospace">Reaction</text>
  <text x="452" y="175" text-anchor="end" fill="#6e6e73" font-size="12">▾</text>

  <rect x="32" y="196" width="436" height="34" rx="6" fill="none" stroke="#0071e3" stroke-width="2"/>
  <text x="44" y="217" fill="#6e6e73" font-size="12">Segment Tab</text>
  <text x="210" y="217" fill="#1d1d1f" font-size="12" font-family="ui-monospace, Consolas, monospace">Scheme tab</text>
  <text x="452" y="217" text-anchor="end" fill="#6e6e73" font-size="12">▾</text>

  <rect x="32" y="238" width="436" height="34" rx="6" fill="none" stroke="#0071e3" stroke-width="2"/>
  <text x="44" y="259" fill="#6e6e73" font-size="12">Reaction Type</text>
  <text x="210" y="259" fill="#1d1d1f" font-size="12" font-family="ui-monospace, Consolas, monospace">Interaction</text>
  <text x="452" y="259" text-anchor="end" fill="#6e6e73" font-size="12">▾</text>

  <line x1="20" y1="292" x2="480" y2="292" stroke="#d2d2d7" stroke-width="1.3"/>
  <rect x="246" y="308" width="96" height="34" rx="7" fill="none" stroke="#d2d2d7" stroke-width="1.3"/>
  <text x="294" y="330" text-anchor="middle" fill="#1d1d1f" font-size="13">Cancel</text>
  <rect x="356" y="308" width="112" height="34" rx="7" fill="#0071e3"/>
  <text x="412" y="330" text-anchor="middle" fill="#ffffff" font-size="13" font-weight="600">Update</text>
</svg>
</div>

The two highlighted rows are new. **Segment Tab**'s options depend on the element you picked above — *Scheme tab* only appears for Reaction, other elements offer *Properties tab*. **Reaction Type** (or **Sample Type**) is hidden entirely whenever Segment Tab is *New (own tab)*, since an own-tab segment always applies to every variant.
{: .fs-2 .mb-0 .text-center }

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## Example Scenario

1. In the **Segment Designer**, create a **new segment** and set **Assign to Element** to Reaction — this choice is only made at creation; an existing segment can't be reassigned to a different element later.
2. Set **Segment Tab** to *Scheme tab*, and optionally **Reaction Type** to *Interaction*.
3. Create a template for that segment, then **Save and Release** as usual.
4. Open a reaction of type **Interaction** — the segment now appears stacked inside the **Scheme** tab instead of on its own. Switch the reaction to **Standard** and it disappears; switch back and it's there again, data intact.

[⬆ Back to top](#table-of-contents)
{: .text-right .fs-2 }

---

## How It Works

- **A per-segment choice.** Placement and variant are set per segment template in the Designer, not as a global setting, and travel with the segment's releases.
- **Nothing breaks.** Segments and templates from before this release keep working unchanged, as their own tab.

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
