---
type: page
title: Unlisting
listed: false
slug: unlisting-old
description: 
index_title: Unlisting
hidden: 
keywords: 
tags: 
---

An unlisted page is a page that your readers can not see yet or reach. It can only be edited by your teammates.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1566173703/18830/kvovikgj0qbgbo4kbvmm.png" caption="Unlisted Page" mode="responsive" height="1834" width="2740" %}
{% /image %}

## How could a Page get Unlisted?

A page can be unlisted because:

- It was never published yet. After a page is created and first saved as a draft, it would still be unlisted until first published.
- A teammate has unlisted the page.
- If it is a subpage, a teammate has unlisted its parent page.

## How to Unlist a Page?

To unlist a page that is listed:

- In the index, open the **Options** {% icon classes="fas fa-ellipsis-v" /%} menu for the page to be unlisted.
- Click on **Unlist** {% icon classes="fas fa-eye-slash" /%}.

To list the page back again:

- In the index, open the **Options** {% icon classes="fas fa-ellipsis-v" /%} menu for the page to be unlisted.
- Click on **List** {% icon classes="fas fa-eye" /%}.

## Hiding Page

If you wish to hide a page from the index, but keep it available for readers if they access it through a URL or a [page link](/support-center/page-linking), then you can do so using [Custom CSS](/support-center/custom-css). Every item in the index has specific CSS classes that help you apply certain CSS rules to it. For example, to hide this page from the index, we can use:

{% code %}
{% tab language="css" %}
.customise.live .node_<page_id> {
  display: none;
}
{% /tab %}
{% /code %}

{% callout type="warning" title="Warning" %}
Making sure to use `.live` CSS class, otherwise you will not be able to see or modify the index in the editor as well.
{% /callout %}