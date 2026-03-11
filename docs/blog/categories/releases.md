---
layout: default
title: Releases
parent: Categories
grand_parent: Blog
nav_order: 2
has_children: true
permalink: /blog/categories/releases
categories: [Releases]
---

# Releases
{: .fw-500 }

{% assign page_files = site.pages | where_exp: "item", "item.categories contains 'Releases'" %}
{% assign sorted_posts = page_files | sort: 'date' | reverse %}

{% for post in sorted_posts %}
  <article class="post-preview mb-5">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <time datetime="{{ post.date | date_to_xmlschema }}" class="fs-3 fw-500">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.description %}
      <p class="mt-2 fs-3">{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}
