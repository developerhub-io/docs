---
type: page
title: Icons
listed: true
slug: icons
description: 
index_title: Icons
hidden: 
keywords: 
tags: inline-blocks
---

Add Font Awesome icons to your pages. Font Awesome 5.15.4 free is loaded.

## How to add an Icon?

To add an icon, start typing "/" and choose **Icon** from the inline blocks list.

## Icon Examples

- Database {% icon classes="fas fa-database" /%}
- User {% icon classes="fas fa-user" /%}

## Styling Icons

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

To style icons, you can provide CSS in [Custom CSS](/support-center/custom-css), and supply the class used in Classes option when editing the icon. For example:

- Icon with primary colour (already available) {% icon classes="fas fa-rocket primary-text" /%} by applying `primary-text` class.
- Icon with primary background (already available) {% icon classes="fas fa-check-circle primary-background" /%} by applying `primary-background` class.
- Icon with a different background colour using the following CSS:

{% code %}
{% tab language="css" title="CSS" %}
.custom-icon.blue-bg {
  background: blue;
  color: white;
  padding: 2px;
}
{% /tab %}
{% /code %}