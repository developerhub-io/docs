---
type: page
title: Badges
listed: true
slug: badges
description: 
index_title: Badges
hidden: 
keywords: 
tags: inline-blocks
---

Badges provide labelling and are a part of %product%'s inline blocks.

## How to add a Badge?

To add a badge, start typing "/" and choose **Badge** from the inline block list.

## Badge Examples

{% badge text="Primary" type="primary" /%} {% badge text="Success" type="success" /%} {% badge text="Warning" type="warning" /%} {% badge text="Info" /%} {% badge text="Error" type="error" /%} {% badge text="Custom" type="custom" /%}

## Advanced Configuration

Custom badge could be modified through [Custom CSS](/support-center/custom-css) to be any colour you want, or even depending on the content it has:

{% code %}
```css {% title="Custom CSS" %}
.customise .cbadge.custom[data-text="Pink Badge"] {
  color: white !important;
  background: #ff536b !important;
}

.customise .cbadge.custom[data-text="Purple Badge"] {
  color: white !important;
  background: #6d53ff !important;
}
```
{% /code %}

Would yield {% badge text="Pink Badge" type="custom" /%} and {% badge text="Purple Badge" type="custom" /%}.
