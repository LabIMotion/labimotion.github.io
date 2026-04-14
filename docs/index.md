---
layout: home
title: Home
nav_order: 1
permalink: /
---

<div class="apple-hero-light" markdown="1">

# LabIMotion Blog

Standardize your lab data with flexibility — updates, releases, and feature deep dives written for researchers.

[Try LabIMotion](https://labimotion-stage.ibcs.kit.edu/home){: .btn .btn-primary }
[View on GitHub](https://github.com/LabIMotion/labimotion){: .btn }
[View Template Hub](https://www.chemotion-repository.net/home/genericHub){: .btn }

</div>


## Latest Updates

{% assign all_pages = site.pages %}
{% assign blog_posts = "" | split: "" %}

{% for page in all_pages %}
  {% assign path_segments = page.path | split: '/' %}
  {% if path_segments.size > 3 and path_segments[0] == 'blog' and path_segments[1] == 'categories' %}
    {% if page.date and page.name != 'index.md' %}
      {% unless page.title == 'Announcements' or page.title == 'Releases' or page.title == 'Preview' %}
        {% assign blog_posts = blog_posts | push: page %}
      {% endunless %}
    {% endif %}
  {% endif %}
{% endfor %}

{% assign sorted_posts = blog_posts | sort: 'date' | reverse %}

{% for post in sorted_posts limit:3 %}
  {% include post-preview.html post=post show_categories=true %}
{% endfor %}

[View All Posts](./blog/archive) | [Browse by Category](./blog/categories)

## Feedback

We value your feedback on any challenges you're facing with the current version or suggestions for improvement. Feel free to share your thoughts with us via email.

[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-primary }

## Newsletter

Subscribe to stay updated on the latest developments, tips, and best practices.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-primary }
