---
layout: default
title: Categories
nav_order: 2
has_children: true
has_toc: false
permalink: /blog/categories
---

<div class="apple-hero-light" markdown="1">

# Categories

Browse posts by topic.

</div>

{% assign all_posts = site.pages | where_exp: "item", "item.path contains 'blog/categories/'" | where_exp: "item", "item.name != 'index.md'" | where_exp: "item", "item.date" %}

{% assign announcements_count = all_posts | where_exp: "item", "item.categories contains 'Announcements'" | size %}
{% assign releases_count = all_posts | where_exp: "item", "item.categories contains 'Releases'" | size %}
{% assign highlights_count = all_posts | where_exp: "item", "item.categories contains 'Feature Highlights'" | size %}
{% assign preview_count = all_posts | where_exp: "item", "item.categories contains 'Preview'" | size %}

<div class="apple-card-grid">
  <div class="apple-card">
    <a class="apple-card-link" href="{{ '/blog/categories/announcements' | relative_url }}" aria-label="Browse Announcements">Announcements</a>
    <p class="apple-card-eyebrow">{{ announcements_count }} posts</p>
    <div class="apple-card-title">Announcements</div>
    <p class="apple-card-desc">Project news, community milestones, and important communications.</p>
    <span class="apple-card-cta">Browse announcements</span>
  </div>

  <div class="apple-card">
    <a class="apple-card-link" href="{{ '/blog/categories/releases' | relative_url }}" aria-label="Browse Releases">Releases</a>
    <p class="apple-card-eyebrow">{{ releases_count }} posts</p>
    <div class="apple-card-title">Releases</div>
    <p class="apple-card-desc">Versioned release notes — what's new, fixed, and improved in each build.</p>
    <span class="apple-card-cta">Browse releases</span>
  </div>

  <div class="apple-card">
    <a class="apple-card-link" href="{{ '/blog/categories/feature-highlights' | relative_url }}" aria-label="Browse Feature Highlights">Feature Highlights</a>
    <p class="apple-card-eyebrow">{{ highlights_count }} posts</p>
    <div class="apple-card-title">Feature Highlights</div>
    <p class="apple-card-desc">Deep dives into capabilities that make LabIMotion productive for everyday lab work.</p>
    <span class="apple-card-cta">Browse highlights</span>
  </div>

  <div class="apple-card">
    <a class="apple-card-link" href="{{ '/blog/categories/preview' | relative_url }}" aria-label="Browse Preview">Preview</a>
    <p class="apple-card-eyebrow">{{ preview_count }} posts</p>
    <div class="apple-card-title">Preview</div>
    <p class="apple-card-desc">Early looks at upcoming features and experimental capabilities.</p>
    <span class="apple-card-cta">Browse previews</span>
  </div>
</div>
