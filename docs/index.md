---
layout: home
title: Home
nav_order: 1
permalink: /
---

# LabIMotion Blog
{: .fs-9 .fw-700 }

The LabIMotion Blog shares updates and insights to help you standardize your laboratory data with flexibility.
{: .fs-6 .fw-300 }

![LabIMotion Blog](assets/images/labimotion_logo.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }

[Try LabIMotion](https://labimotion-stage.ibcs.kit.edu/home){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 }
[View on GitHub](https://github.com/LabIMotion/labimotion){: .btn .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View Template Hub](https://www.chemotion-repository.net/home/genericHub){: .btn .fs-5 .mb-4 .mb-md-0 }

---

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
  <article class="post-preview mb-6">
    {% if post.categories %}
    <div class="post-categories mt-6">
      {% for category in post.categories %}
        <a href="{{ site.baseurl }}/blog/categories/{{ category | slugify | downcase }}" class="category-tag">{{ category }}</a>
      {% endfor %}
    </div>
    {% endif %}
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    {% if post.description %}
      <p class="mb-1">{{ post.description }}</p>
    {% endif %}
    <time datetime="{{ post.date | date_to_xmlschema }}" class="fs-3 fw-500">{{ post.date | date: "%B %d, %Y" }}</time>
  </article>
{% endfor %}

[View All Posts](./blog/archive) | [Browse by Category](./blog/categories)

## Feedback

We value your feedback on any challenges you're facing with the current version or suggestions for improvement. Feel free to share your thoughts with us via email.

[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-primary }

## Newsletter

Subscribe to stay updated on the latest developments, tips, and best practices.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-primary }
