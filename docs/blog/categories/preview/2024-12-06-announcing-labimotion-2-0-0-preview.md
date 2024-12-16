---
layout: default
title: "Version 2.0.0 Public Preview"
date: 2024-12-06
author: "Claire Lin"
parent: Preview
grand_parent: Categories
nav_exclude: false
nav_order: -20241206
categories: [Announcements, Preview]
description: "This is a significant milestone for LabIMotion as we are upgrading to the latest version of react-bootstrap, the main library for UI components. We have also introduced new features to enhance the user experience."

---

# Chemotion LabIMotion 2.0.0 Preview Start!
{: .fw-500 }

{% include post-header.html
  description=page.description
  author=page.author
  date=page.date
%}

Dear Chemotion LabIMotion users,

Welcome to the preview for Chemotion LabIMotion 2.0.0!

This is a major milestone for LabIMotion as we are upgrading to the latest version of react-bootstrap, which is the main library for UI components. This upgrade brings us a more modern and feature-rich UI experience.

With the new version of react-bootstrap and feedback from the community, we've also introduced new features to enhance the user experience. Let's jump into the details!

## Introducing the new UI experience

### Designer's New Form Layout

Based on community feedback, we have redesigned the form layout with a more general style to make it easier for users to get started.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Form Layout](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/form-layout.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/form-layout.png){:target="_blank"}
{: .mt-0 }

### Arranging the order

Drag-and-drop is a highly interactive and user-friendly feature. We use drag-and-drop to perform reordering layers or fields for Designer, and the similar feature for User to rearrange the layers in the workspace. Reordering is great, but it's even better if the user can compare the original order at the same time. Therefore, we have provided a dedicated feature for ordering that allows you to visually compare the original order and the new order.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: center; margin-top: 0;">
  <a href="/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/arrange-layers.mp4" target="_blank" style="display: block;">
    <video width="75%" controls autoplay loop muted>
      <source src="/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/arrange-layers.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </a>
</div>

As a Designer, you can find functions to reorder layers or fields accordingly.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

[![Arrange for Designer](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/arrange-for-designer.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/arrange-for-designer.png){:target="_blank"}
{: .mt-0 }

In user workspace (aka `MyDB`), you can find a button called `Arrange` on the toolbar and use it to rearrange layers.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }
[![Arrange for User](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/arrange-for-user.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/arrange-for-user.png){:target="_blank"}
{: .mt-0 }

## Workflow for Segment

In this version, we have introduced the workflow functionality to Segment. As a Designer, you can define a workflow in Segment template just like in Element template.

<!-- <div class="alert alert-info" role="alert">
  <i class="bi bi-info-circle-fill"></i> For more details about the workflow feature, please refer to the <a href="https://www.chemotion.net/docs/labimotion/guides/designer/workflow">Designer Guide</a>.
</div> -->

> <i class="bi bi-info-circle-fill"></i>
> For more details about the workflow feature, please refer to the [Designer Guide](https://www.chemotion.net/docs/labimotion/guides/designer/workflow).

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }
[![Workflow for Segment Designer](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/workflow-segment-designer.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/workflow-segment-designer.png){:target="_blank"}
{: .mt-0 }

When you use a Segment that contains a predefined workflow, the workflow is automatically applied to the Segment and you can click the `Workflow (Predefined)` button to view the defined workflow.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }
[![Workflow for Segment User](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/workflow-segment-user.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/workflow-segment-user.png){:target="_blank"}
{: .mt-0 }

## Vocabularies and Standard Layers Updates

In the initial release of the LabIMotion Vocabulary (Lab-Vocab) and Standard Layer, the data size were relatively small. Developing uniform, predefined, reusable, ontology-related sets of fields and layouts is a complex task that relies on domain expertise. We are grateful to the community for their invaluable contributions, which allow us to continuously enhance this data.

(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }
[![Vocab and Standard Layers Example](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/generic-vocab-and-layers_dataset-example.png){: .mx-auto .d-block .mb-4 .img-fluid .w-75 }](/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/generic-vocab-and-layers_dataset-example.png){:target="_blank"}
{: .mt-0 }


(Click to view in a new window <i class="bi bi-window"></i>)
{: .fs-2 .mb-0 }

<div style="display: flex; justify-content: center; margin-top: 0;">
  <a href="/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/generic-vocab-and-layers.mp4" target="_blank" style="display: block;">
    <video width="75%" controls autoplay loop muted>
      <source src="/assets/images/posts/2024-12-06-announcing-labimotion-2-0-0-preview/generic-vocab-and-layers.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </a>
</div>

<br>

---

### How to Participate in the Preview

1. 🖥️ **Visit the Test Instance:** [Link to Test Instance](https://labimotion-stage.ibcs.kit.edu/home)
2. 🔍 **Explore the New Features:** Dive into the new functionalities and see how they enhance your workflow.
3. ❤️ **Provide Feedback:** For the feedback of this preview, please share your thoughts and observations in our discussion thread [Link to Discussion Thread](https://github.com/LabIMotion/labimotion/discussions/39).

We appreciate your participation and look forward to your feedback.

Thank you!

{% include category-tags.html categories=page.categories %}

{% include subscribe-feedback.html %}
