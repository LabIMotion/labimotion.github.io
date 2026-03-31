---
layout: default
title: "Version 2.1.1 Patch Release"
date: 2026-03-25
author: "Claire Lin"
parent: Releases
grand_parent: Categories
nav_exclude: false
nav_order: -20260325
categories: [Announcements, Releases]
description: This patch release includes important fixes, minor usability enhancements, and dependency updates to improve stability and maintainability.
---

# 🔧 LabIMotion 2.1.1 Patch Release

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

We are pleased to announce this latest patch release, **LabIMotion 2.1.1**, focused on stability, maintenance, and a small set of experimental usability enhancements.

This update includes fixes for designer draft saving and element creation in the “All” collection, along with two small usability improvements: support for the A/mm² unit and automatic expansion of the first group by default.

Key updates include:

- **Designer Draft Saving Fix** – Resolved an issue where drafts could not be saved after importing a template into the work area.
- **A/mm² Unit Support** – Added A/mm² as a unit for specific current.
- **Default Group Expansion** – The first group is now expanded by default for a smoother user experience.
- **Experimental: Overview Map** – A real-time dashboard tracking progress via color-coded bars and percentages, allowing users to instantly jump to and highlight specific sections using navigation icons.
- **"All" Collection Element Creation (Forward-looking fix)** – Allows creating elements in the “All” collection, adapting to logic introduced in Chemotion ELN v3.x.

This patch release also includes dependency and build updates for improved security and maintenance. A complete list of changes is available in the [Chemotion LabIMotion v2.1.1 Patch Release](https://github.com/LabIMotion/labimotion/discussions/76){:target="_blank" rel="noopener"}.

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
