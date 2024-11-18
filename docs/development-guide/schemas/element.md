---
layout: default
title: Element Schema
parent: Schemas
grand_parent: Development Guide
nav_order: 1
---

# Element Schema

{: .text-center .fs-9 }

A standardized set of metadata properties used to describe Elements in LabIMotion.
{: .text-center .fs-6 .fw-300 }

[View JSON Schema]({{ site.baseurl }}/schema/latest/sch-element.json){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View on GitHub](https://github.com/LabIMotion/labimotion/blob/main/src/sch-element.json){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Overview

The Element Schema provides a contract for the JSON data used in LabIMotion elements, detailing what properties the JSON data should have, their types, and additional constraints.

## Schema Structure

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "$id": "https://labimotion.github.io/schema/latest/sch-element.json",
  "type": "object",
  "allOf": [
    {
      "$ref": "./include/sch-common-properties.json"
    },
    {
      "properties": {
        "layers": {
          "$ref": "./include/sch-layers.json"
        }
      }
    }
  ]
}
```

## Properties

### Common Properties

All Element objects must include these common properties:

| Property | Type   | Required | Description                               |
| :------- | :----- | :------- | :---------------------------------------- |
| `pkg`    | Object | Yes      | Package information including ELN version |
| `uuid`   | String | Yes      | Unique identifier                         |
| `klass`  | String | Yes      | Must be "ElementKlass"                    |

### Layer Properties

Elements can have multiple layers, each containing:

| Property   | Type    | Required | Description                          |
| :--------- | :------ | :------- | :----------------------------------- |
| `key`      | String  | Yes      | Layer identifier                     |
| `cols`     | Integer | Yes      | Number of columns                    |
| `position` | Integer | Yes      | Layer position                       |
| `fields`   | Array   | No       | Array of fields                      |
| `color`    | String  | No       | Background color of the layer header |
| `label`    | String  | No       | Label of the layer                   |

## Example

```json
{
  "pkg": {
    "eln": {
      "version": "1.0.0",
      "base_revision": "1",
      "current_revision": "1"
    },
    "labimotion": "1.0.0"
  },
  "uuid": "123e4567-e89b-12d3-a456-426614174000",
  "klass": "ElementKlass",
  "layers": {
    "basic": {
      "key": "basic",
      "cols": 2,
      "position": 1,
      "fields": []
    }
  }
}
```

## Related Schemas

- [Common Properties Schema](../common-properties)
- [Layers Schema](../layers)

## Version History

### Version 1.0 (Current)

- Released: January 31, 2024
- Initial release with basic element structure
- Layer support
- Field definitions

## Feedback

We appreciate your feedback regarding any challenges you may be facing with the current schema or any ideas you have for improvements.

[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
[<i class="bi bi-github"></i> GitHub](https://github.com/LabIMotion/labimotion){: .btn .btn-blue }
