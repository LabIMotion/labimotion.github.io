---
layout: default
title: "LabIMotion 1.5.0 Public Preview"
date: 2024-10-05
parent: Blog
categories: [Announcements, Preview]
description: "Join the preview of Chemotion LabIMotion 1.5.0 and explore exciting new features including vocabulary enhancements, generic layer support, and UI foundation improvements."
---

<h1 class="fw-500">🎉 Chemotion LabIMotion 1.5.0 Preview!</h1>

<time datetime="{{ page.date | date_to_xmlschema }}" class="fw-500">{{ page.date | date: "%B %d, %Y" }}</time>

Dear Chemotion LabIMotion users,

We're excited to share the upcoming features we've prepared. Please feel free to explore these enhancements in our [test instance](https://labimotion-stage.ibcs.kit.edu/home) and share your thoughts and observations in our discussion thread.

### What's New in v1.5.0:

- 🔤 **Vocabulary**

- 🧱 **Generic Layer**

- ✍️ **UI Foundation**

All details and videos are available at [here](https://github.com/LabIMotion/labimotion/discussions/37).

### How to Participate:

1. 🖥️ **Visit the Test Instance:** [Link to Test Instance](https://labimotion-stage.ibcs.kit.edu/home)
2. 🔍 **Explore the New Features:** Dive into the new functionalities and see how they enhance your workflow.
3. 💬 **Provide Feedback:** Share your thoughts and observations in our discussion thread [Link to Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/37).

We appreciate your participation and look forward to your feedback.

Thank you!

Best regards,<br>
LabIMotion Team

---

{% if page.categories %}
  <div class="post-categories mt-6">
    Categories:&nbsp;&nbsp;
    {% for category in page.categories %}
      <a href="./categories#{{ category | slugify }}" class="category-tag">{{ category }}</a>
    {% endfor %}
  </div>
{% endif %}

---

### Subscribe & Share Feedback

Get the latest development updates, tips, and best practices, or share your feedback with us.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-blue }
[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
