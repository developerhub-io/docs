---
type: page
title: Merge API Definitions
listed: true
slug: merge-api-definitions
description: 
index_title: Merge API Definitions
hidden: 
keywords: 
tags: 
---

Merging API references lets you combine multiple existing API definitions into a single merged API reference. This is useful when your API surface is split across multiple services or files, but you want readers to browse one consolidated reference.

The merged result is saved as a **draft** API reference so you can review it before publishing.

{% image url="asset:hqcj861fb8nx" mode="responsive" height="1190" width="1720" %}
{% /image %}

## Merge API References

To create a merged API reference:

- Open **References** {% icon classes="fas fa-vector-square inv-icon" /%} from the sidebar.
- Select **Merge API References**.
- (Optional) Add an **Override API Reference**.
- Select the API references you want to merge from the list (from the current version).
- Set the merge order using the **up** and **down** arrows next to each reference.
- Click **Merge**. The merged API reference will be created in **draft** state.

## Override API Reference

The **Override API Reference** is an optional OpenAPI definition that takes precedence over everything else in the merge. It can be provided in **JSON or YAML** format. Use it to override specific parts of the merged output, for example:

- `info` (including `title`, `description`, and `version`)
- Any components, schemas, and security definitions that you want to win in case of conflicts

{% callout type="info" title="OpenAPI Version Is Required" %}
The Override API Reference must include the `openapi` version. In practice, it is also expected that `info`, `description`, and `version` are overridden here.
{% /callout %}

### Example Override API Reference

{% callout type="info" title="What This Example Does" %}
This override sets the API title and version, and replaces the `bearerAuth` security scheme.
{% /callout %}

{% code %}
{% tab language="yaml" title="YAML" %}
openapi: 3.0.3
info:
  title: Merged API (Public)
  description: Consolidated reference for all services.
  version: 2026-03-01
components:
  securitySchemes:
    bearerAuth:
      type: http
      scheme: bearer
      bearerFormat: JWT
security:
  - bearerAuth: []
{% /tab %}
{% tab language="json" title="JSON" %}
{
  "openapi": "3.0.3",
  "info": {
    "title": "Merged API (Public)",
    "description": "Consolidated reference for all services.",
    "version": "2026-03-01"
  },
  "components": {
    "securitySchemes": {
      "bearerAuth": {
        "type": "http",
        "scheme": "bearer",
        "bearerFormat": "JWT"
      }
    }
  },
  "security": [
    { "bearerAuth": [] }
  ]
}
{% /tab %}
{% /code %}

## Merge Order and Precedence

You can choose from the API references that already exist in the version you are currently editing.

Precedence is determined by the list order:

- References earlier in the list take precedence.
- References later in the list (higher order number) overwrite earlier ones when there is a conflict.

Conflicts are resolved by name. If the same name exists in multiple references, later references overwrite earlier ones, for example:

- Components
- Schemas
- Security schemes (and other security-related named objects)

To change precedence, use the **up** and **down** arrows next to each reference in the list.

## Requirements

- All API definitions in the merge must use the exact same OpenAPI version.