---
type: page
title: OpenAPI Extensions
listed: true
slug: openapi-extensions
description: 
index_title: OpenAPI Extensions
hidden: 
keywords: 
tags: 
---

The following extensions are available on %product%.

## x-tagGroups

`x-tagGroups` groups operations in the index, creating one further hierarchy. This feature is only enabled if the  [index is set to be collapsible](/support-center/api-reference-settings#allow-index-to-collapse).

Tag groups can be defined as such in OpenAPI:

{% code %}
{% tab language="yaml" %}
openapi: '3.0'
info: ...
tags:
  - name: Lion
  - name: Cheetah
  - name: Dolphin
  - name: Octopus
x-tagGroups:
  - name: Feline
    tags:
      - Lion
      - Cheetah
  - name: Sea
    tags:
      - Dolphin
      - Octopus
{% /tab %}
{% /code %}

## x-enum-varnames

`x-enum-varnames` gives a secondary name for an enum.

Enum var names can be defined as such in OpenAPI:

{% code %}
{% tab language="yaml" title="" %}
Animal:
  type: integer
  enum:
    - 33
    - 21
  x-enum-varnames:
    - Dog
    - Cat
{% /tab %}
{% /code %}

## Variables

In addition to using [variables](/support-center/variables) throughout the API references, those variables can also be used:

- `%_.project.base_path%` for project base path.
- `%_.version.slug%` for version slug.
- `%_.section.slug%` for API reference slug.

Those variables are specifically useful to construct links inside markdown descriptions.

## x-labels

`x-labels` adds one or more labels to a schema property's description.

Labels can be defined as such in OpenAPI:

{% code %}
{% tab language="yaml" highlightLines="17-21" %}
"/documentation/{id}/page":
  post:
    requestBody:
      content:
        application/json:
          schema:
            description: Page object
            required:
              - title
              - content
            type: object
            properties:
              title:
                description: Title of the page
                type: string
              content:
                x-labels:
                  - text: New
                    type: green-badge
                  - text: Private
                    type: red-badge
                description: >-
                  Draft contents of the page in [Darkdown
                  format](https://docs.developerhub.io/support-center/exporting-documentation#darkdown)
                type: string
{% /tab %}
{% /code %}

When `x-labels` is set, each label is placed in the description, unstyled, using the text provided. Each label is given the CSS classes `label` and `type` specified. This can be used to add specific labels with specific colours, like badges on a description.