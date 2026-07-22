---
type: page
title: Callouts
listed: true
description: 
index_title: Callouts
hidden: false
keywords: 
tags: blocks
---

Callouts are pieces of information that standout from normal text to notify the user. They change colour according to their type.

To create a callout:

{% synced id="open-block-menu" /%}

- Select Callout {% icon classes="fas fa-exclamation" /%}

## Types

Callouts have the following types:

- Info
- Warning
- Success
- Error

To change a callout's type, click its icon and pick the type you want. The colour updates to match.

## Fields

A callout has an optional title and its contents. Use **Add title** to show the title row, or **Remove title** to hide it and keep just the body.

## Callout Example

{% callout type="success" title="Success" %}
Great **success**!
{% /callout %}

{% callout type="warning" title="Warning" %}
Woah, watch out!
{% /callout %}

{% callout title="Info" %}
Informative callout
{% /callout %}

{% callout type="error" title="Error" %}
This doesn't look right
{% /callout %}
