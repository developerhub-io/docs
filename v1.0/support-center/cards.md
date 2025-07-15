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

A card layout can fit in its width a maximum of 3 cards. Each card has a title, text and link. The link can be internal or external. Internal links should look like `/support-center/cards`, `/api`, or `/custom-page` and should not include the project's basepath or the version.

## Cards Example

{% cards %}
{% card title="Synced Blocks" link="/support-center/synced-blocks" %}
Single-sourcing tool to write content once and use it multiple times
{% /card %}
{% card title="Tabs" link="/support-center/tabs" %}
Split content into multiple tabs for ease of reading
{% /card %}
{% card title="Custom HTML" link="https://example.com" %}
Add anything to the page. Anything at all!
{% /card %}
{% /cards %}