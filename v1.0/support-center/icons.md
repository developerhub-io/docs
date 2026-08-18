---
type: page
title: Icons
listed: true
description: 
index_title: Icons
hidden: false
keywords: 
tags: inline-blocks
---

Add Font Awesome icons to your pages. Font Awesome 7 Free is loaded, giving you the Solid, Regular, and Brands styles.

## How to add an Icon?

To add an icon, start typing "/" and choose **Icon** from the inline blocks list.

To put an icon next to an entry in your navigation index instead, see [Index Icons](structuring-documentation/index-icons.md).

## Icon Examples

- Database {% icon classes="fas fa-database" /%}
- User {% icon classes="fas fa-user" /%}

## Styling Icons

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Pro Projects
</div>
{% /html %}

To style icons, you can provide CSS in [Custom CSS](customising-visuals/custom-css.md), and supply the class used in Classes option when editing the icon. For example:

- Icon with primary colour (already available) {% icon classes="fas fa-rocket primary-text" /%} by applying `primary-text` class.
- Icon with primary background (already available) {% icon classes="fas fa-check-circle primary-background" /%} by applying `primary-background` class.
- Icon with a different background colour using the following CSS:

{% code %}
```css {% title="CSS" %}
.custom-icon.blue-bg {
  background: blue;
  color: white;
  padding: 2px;
}
```
{% /code %}
