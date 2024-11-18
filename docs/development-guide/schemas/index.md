---
layout: default
title: Schemas
parent: Development Guide
has_children: true
nav_order: 1
---

# LabIMotion Schemas

Documentation for all available LabIMotion JSON Schemas.

## Available Schemas

### Core Schemas

| Schema                      | Description                        | Version |
| :-------------------------- | :--------------------------------- | :------ |
| [Element Schema](./element) | Defines the structure for elements | 1.0     |
| [Segment Schema](./segment) | Defines the structure for segments | 1.0     |
| [Dataset Schema](./dataset) | Defines the structure for datasets | 1.0     |

### Supporting Schemas

| Schema                                   | Description                             |
| :--------------------------------------- | :-------------------------------------- |
| [Common Properties](./common-properties) | Base properties used across all schemas |
| [Layers](./layers)                       | Layer structure definition              |
| [Fields](./fields)                       | Field type definitions                  |

## Schema Versioning

The current stable version is 1.0. All schemas follow semantic versioning:

- Major version changes (1.0 → 2.0) indicate breaking changes
- Minor version changes (1.0 → 1.1) indicate new features
- Patch version changes (1.0.0 → 1.0.1) indicate bug fixes

## Using the Schemas

### Direct References

You can reference the schemas directly in your JSON:

```json
{
  "$schema": "https://labimotion.github.io/schema/v1.0/sch-element.json"
}
```

## Contributing

We welcome contributions! Please see our [contribution guidelines](../contributing) for more information.
