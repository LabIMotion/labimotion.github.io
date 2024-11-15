---
layout: default
title: Element Schema
parent: Schemas
nav_order: 1
---

# Element Schema

{: .no_toc }

## Table of contents

{: .no_toc .text-delta }

1. TOC
   {:toc}

## Overview

The Element Schema defines the basic structure for LabIMotion elements. It extends the common properties and adds specific element-related fields.

## Schema Definition

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
