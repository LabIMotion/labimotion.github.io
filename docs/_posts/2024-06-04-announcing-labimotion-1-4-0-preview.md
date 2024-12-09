---
layout: default
title: "LabIMotion 1.4.0 Public Preview"
date: 2024-06-04
author: "Claire Lin"
parent: Blog
categories: [Announcements, Preview]
description: "Join the preview of Chemotion LabIMotion 1.4.0 and explore exciting new features including image previews, custom labeling, and interactive workflows."
---

# Preview Start! Join the Chemotion LabIMotion 1.4.0 Preview! 👀
{: .fw-500 }

<span class="fs-3">{{ page.description }}<span>

<span class="fw-500">{{ page.author }}</span><span class="mx-2 fw-500">·</span><time datetime="{{ page.date | date_to_xmlschema }}" class="fw-500">{{ page.date | date: "%B %d, %Y" }}</time>

<hr style="border-top: 1px solid #0d6efd;">

Dear Chemotion LabIMotion users,

We are thrilled to announce the upcoming release of Chemotion LabIMotion version 1.4.0! To ensure this version meets your needs and expectations, we invite you to participate in our preview program. This is your chance to explore the new features and provide invaluable feedback.

### What's New in v1.4.0:

* 🖼️ **Preview Image Function for the "Upload" Field Type:** Get an image preview as soon as you upload a file. You can zoom in/out by adjusting the percentage, and open the original file with a single click.

* 🏷️ **Labeling Feature:** Enhance your organization and categorization with custom labels. This feature improves searchability and overall management within the system.

* ➡️ **Drag Reactions to Elements:** Experience a more interactive and intuitive interface by dragging and dropping reactions onto elements. The Export/Import Collection and Reporting functions will now include reaction data as well.

* 🔄 **Change Layer or Field Order via Drag-and-Drop:** Enjoy greater flexibility in managing your data by simply dragging and dropping layers or fields into your desired order.

* 🖌️ **Custom Flow:** Enables users to record their steps/work and visualize them as a flow diagram.

All details and videos are available at [here](https://github.com/LabIMotion/labimotion/discussions/30).

We encourage you to try out these features in our test instance and share your feedback or observations. Your insights are crucial for refining these features before the final release.

### How to Participate:
1. 🖥️ **Visit the Test Instance:** [Link to Test Instance](https://labimotion-stage.ibcs.kit.edu/home)
2. 🔍 **Explore the New Features:** Dive into the new functionalities and see how they enhance your workflow.
3. 💬 **Provide Feedback:** Share your thoughts and observations in our discussion thread [Link to Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/29).

We appreciate your participation and look forward to your feedback.

Thank you!

---

{% if page.categories %}
  <div class="post-categories mt-6">
    Categories:&nbsp;&nbsp;
    {% for category in page.categories %}
      <a href="/blog/categories#{{ category | slugify }}" class="category-tag">{{ category }}</a>
    {% endfor %}
  </div>
{% endif %}

---

### Subscribe & Share Feedback

Get the latest development updates, tips, and best practices, or share your feedback with us.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-blue }
[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
