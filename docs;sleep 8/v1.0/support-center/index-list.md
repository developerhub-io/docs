---
type: page
title: Index List
listed: true
slug: index-list
description: 
index_title: Index List
hidden: 
keywords: 
tags: blocks
---

Index list provides a quick way to list all pages under a parent page.

To create an index list:

{% synced id="open-block-menu" %}
{% /synced %}

- Choose Index List {% icon classes="fas fa-list" /%}

A bulleted list containing all child pages, titled and linked, would populate. The list changes dynamically when child pages are added or removed.

{% callout type="info" title="Info" %}
If the page has no child pages, then nothing would show for the readers, as if the block doesn't even exist.
{% /callout %}

## Example Index List

This is an up-to-date list of this page's child pages:

{% index-list %}
{% /index-list %}

Doesn't look any different? Correct, that's the point! But it is auto-generated.