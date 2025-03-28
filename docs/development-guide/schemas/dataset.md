---
layout: default
title: Dataset Schema
parent: Schemas
grand_parent: Development Guide
nav_order: 3
---

# Dataset Schema

{: .text-center .fs-9 }

A standardized set of metadata properties used to describe Datasets in LabIMotion.
{: .text-center .fs-6 .fw-300 }

[View JSON Schema]({{ site.baseurl }}/schema/latest/sch-dataset.json){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View on GitHub](https://github.com/LabIMotion/labimotion/blob/main/src/sch-dataset.json){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Overview

The Dataset Schema provides a contract for the JSON data used in LabIMotion datasets, detailing what properties the JSON data should have, their types, and additional constraints.

## Schema Structure

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "$id": "https://labimotion.github.io/schema/v1.0/sch-dataset.json",
  "type": "object",
  "allOf": [
    {
      "$ref": "./include/sch-common-properties.json"
    },
    {
      "properties": {
        "layers": {
          "$ref": "./include/sch-layers.json",
          "description": "Layers to be used for dataset."
        },
        "select_options": {
          "$ref": "./include/sch-select-options.json",
          "description": "Select options for dataset."
        }
      }
    }
  ]
}
```

## Properties

### Common Properties

All Dataset objects must include these common properties:

| Property | Type   | Required | Description                               |
| :------- | :----- | :------- | :---------------------------------------- |
| `pkg`    | Object | Yes      | Package information including ELN version |
| `uuid`   | String | Yes      | Unique identifier                         |
| `klass`  | String | Yes      | Must be "DatasetKlass"                    |

### Layer Properties

Datasets can have multiple layers, each containing:

| Property   | Type    | Required | Description                          |
| :--------- | :------ | :------- | :----------------------------------- |
| `key`      | String  | Yes      | Layer identifier                     |
| `cols`     | Integer | Yes      | Number of columns                    |
| `position` | Integer | Yes      | Layer position                       |
| `fields`   | Array   | No       | Array of fields                      |
| `color`    | String  | No       | Background color of the layer header |
| `label`    | String  | No       | Label of the layer                   |

### Select Options

Optional select options for dropdown fields:

| Property  | Type   | Required | Description               |
| :-------- | :----- | :------- | :------------------------ |
| `desc`    | String | Yes      | Description of the option |
| `options` | Array  | Yes      | Array of key-value pairs  |

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
  "klass": "DatasetKlass",
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

- [Common Properties Schema](../../../schema/latest/include/sch-common-properties.json)
- [Layers Schema](../../../schema/latest/include/sch-layers.json)
- [Select Options Schema](../../../schema/latest/include/select-options.json)

## Version History

### Version 1.0 (Current)

- Released: January 31, 2024
- Initial release with basic dataset structure
- Layer support
- Select options support

## Feedback

We appreciate your feedback regarding any challenges you may be facing with the current schema or any ideas you have for improvements.

[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
[<i class="bi bi-github"></i> GitHub](https://github.com/LabIMotion/labimotion){: .btn .btn-blue }
