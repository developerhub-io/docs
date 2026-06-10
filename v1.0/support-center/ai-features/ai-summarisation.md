---
type: page
title: AI SEO Helper
listed: true
slug: ai-summarisation
description: Discover how to use AI summarization to generate META descriptions for your pages. Our beta feature simplifies tasks using OpenAI, with the option to modify descriptions as needed.
index_title: AI SEO Helper
hidden: 
keywords: 
tags: ai
---

Simplify generating a useful META description of pages using AI. This feature uses OpenAI GPT models.

## How to use AI SEO Helper?

To use an AI generated META description of a page:

- Open the page in the editor.
- Click on {% icon classes="fas fa-info-circle" /%} **Page Info** in the right sidebar.
- Open the **Settings** tab. Next to **Description**, click **AI Generate**. It will take a few seconds.
- You may modify the description if needed.
- Click Save.

{% image url="asset:x9dj0mdnmf00" caption="Generating a meta description from the Settings tab" mode="responsive" height="476" width="464" %}
{% /image %}

## What data is sent to the LLM?

When generating META descriptions for a page, a plain text version of the page content is sent to the LLM. If the page is in draft mode, the draft content is sent instead.