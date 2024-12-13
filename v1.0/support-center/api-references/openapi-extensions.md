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