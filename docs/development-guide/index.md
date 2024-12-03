---
layout: default
title: Development Guide
nav_order: 99
has_children: true
permalink: /development-guide
nav_exclude: true
---

# Development Guide
{: .fs-9 }

Learn about LabIMotion templates.
{: .fs-6 .fw-300 }

---

## Overview

The Development Guide provides documentation for working with LabIMotion templates and schemas. This guide will help you understand the structure and capabilities of LabIMotion.

## Getting Started

1. **Understanding Templates**
   - Templates are JSON files that define the structure of your laboratory data
   - Each template follows a specific schema (Element, Segment, or Dataset)
   - Templates can be customized with various field types and layouts

2. **Basic Components**
   - [Element Schema](./schemas/element): A generic element with layers and fields
   - [Segment Schema](./schemas/segment): Groups related data together for a single element
   - [Dataset Schema](./schemas/dataset): A dataset based on the ontology terminology

3. **Template Structure**
   - Each template consists of layers
   - Layers contain fields
   - Fields can be of various types (text, number, select, etc.)

## Template Development

### Prerequisites
- Basic understanding of JSON
- Familiarity with JSON Schema
- Access to the [Template Hub](https://www.chemotion-repository.net/home/genericHub)

### Development Process
1. Choose appropriate schema type
2. Define template structure
3. Add layers and fields
4. Validate against schema
5. Test in LabIMotion
6. Deploy to production

## Best Practices

- Use meaningful layer and field names
- Group related fields in the same layer
- Validate templates before deployment
- Document custom implementations
- Follow naming conventions

## Tools and Resources

- [Template Hub](https://www.chemotion-repository.net/home/genericHub): Browse existing templates
- [JSON Schema Validator](https://www.jsonschemavalidator.net): Validate your templates
- [GitHub Repository](https://github.com/LabIMotion/labimotion): Source code and examples

## Need Help?

We're here to help you with your template development journey:

[<i class="bi bi-envelope-at"></i> Email Support](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
[<i class="bi bi-github"></i> GitHub Issues](https://github.com/LabIMotion/labimotion/issues){: .btn .btn-blue }
