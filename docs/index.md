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

[View on GitHub](https://github.com/LabIMotion/labimotion){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View Template Hub](https://www.chemotion-repository.net/home/genericHub){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Latest Updates

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts limit:1 %}
  <article class="post-preview mb-6">
    {% if post.categories %}
    <div class="post-categories mt-6">
      {% for category in post.categories %}
        <a href="./blog/categories#{{ category | slugify }}" class="category-tag">{{ category }}</a>
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

[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }

## Newsletter

Subscribe to stay updated on the latest developments, tips, and best practices.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-blue }
