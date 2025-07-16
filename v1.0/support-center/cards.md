---
type: page
title: Cards
listed: true
slug: cards
description: 
index_title: Cards
hidden: 
keywords: 
tags: 
---

Cards are a great way to highlight main points and provide links to them.

To create a card layout:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Cards.

You can switch between a grid and list layout by clicking the {% icon classes="fas fa-eye" /%} icon at the top right.

When in grid layout, the card layout can fit in its width a maximum of 3 cards. When in list layout, each card takes the entire width.

Each card has a title, text and link. The link can be internal or external. Internal links should look like `/support-center/cards`, `/api`, or `/custom-page` and should not include the project's basepath or the version.

## Cards Example

Grid layout:

{% cards view="grid" %}
{% card title="Synced Blocks" link="/support-center/synced-blocks" %}
Single-sourcing tool to write content once and use it multiple times
{% /card %}
{% card title="Tabs" link="/support-center/tabs" %}
Split content into multiple tabs for ease of reading
{% /card %}
{% card title="Custom HTML" link="/support-center/custom-html" %}
Add anything to the page. Anything at all!
{% /card %}
{% /cards %}

List layout:

{% cards view="list" %}
{% card title="Synced Blocks" link="/support-center/synced-blocks" %}
Single-sourcing tool to write content once and use it multiple times
{% /card %}
{% card title="Tabs" link="/support-center/tabs" %}
Split content into multiple tabs for ease of reading
{% /card %}
{% card title="Custom HTML" link="/support-center/custom-html" %}
Add anything to the page. Anything at all!
{% /card %}
{% /cards %}