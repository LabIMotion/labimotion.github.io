---
layout: home
title: Home
nav_order: 1
permalink: /
---

# LabIMotion Blog
{: .fs-9 }

The LabIMotion Blog provides information about the LabIMotion project - Standardize your laboratory data with flexibility.
{: .fs-6 .fw-300 }

[View on GitHub](https://github.com/LabIMotion/labimotion){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View Template Hub](https://www.chemotion-repository.net/home/genericHub){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Latest Updates
{: .text-purple-200 }

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts limit:1 %}
  <article class="post-preview">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% endif %}
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.categories %}
    <div class="post-categories">
      {% for category in post.categories %}
        <a href="./categories#{{ category | slugify }}" class="category-tag">{{ category }}</a>
      {% endfor %}
    </div>
    {% endif %}
  </article>
{% endfor %}

[View All Posts](./blog/archive) | [Browse by Category](./blog/categories)

## Subscribe to get the latest updates

[Subscribe to the LabIMotion Newsletter](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-blue }

## Feedback

We appreciate your feedback regarding any challenges you may be facing with the current schema or any ideas you have for improvements.

[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
[<i class="bi bi-github"></i> GitHub](https://github.com/LabIMotion/labimotion){: .btn .btn-blue }
