---
type: page
title: AI Search
listed: true
slug: ai-search
description: 
index_title: AI Search
hidden: 
keywords: 
tags: ai
---

An intelligent assistant that helps readers find answers through natural conversation. This feature uses OpenAI GPT models to provide contextual answers about your documentation and API endpoints.

{% video videoId="https://uploads.developerhub.io/prod/02/nvrnanscgw7okyvlbqfcs8n1xmgxtc6h1cmr54i3e18avestnunznr12liyvk6gx.mp4?autoplay=true&loop=true&muted=true&playsinline=true&controls=false" provider="raw" %}
{% /video %}

## AI Search Features

{% glossary term="AI Search" /%} allows the readers to ask a questions about the docs and API endpoints, delivering GPT-powered responses. Features of AI search: 

- Answers from both documentation and API references.
- Can ask questions in any language, regardless if the documentation is written using that language or not.
- Responds using the language of the question.
- Provides a source list for further reading.
- The reader can ask follow up questions.

## AI Search Experience

When [AI Search is enabled](/support-center/ai-search#enabling-ai-search), an **Ask AI** button appears next to the search bar. Clicking this button opens an assistant sidebar on the right side of the screen.

The assistant provides a conversational interface where readers can:

- Ask questions about the current page they're viewing.
- Ask questions about the documentation in general.
- Ask questions about specific API endpoints.
- Engage in follow-up conversations to clarify or expand on answers.

The assistant responds with detailed explanations and examples when possible, and provides source references for further reading. 

## Enabling AI Search

To enable/disable AI search:

- From the left sidebar, choose **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under AI Features, check or uncheck **Enable AI search**.

Once AI search is enabled, it might take a couple of minutes until it is useable.

## Search Update Frequency

New or deleted content would be effectively available within 30 minutes for AI search.

## Validating Responses

To validate responses provided by AI Search, a log of all questions and answers can be downloaded.

To download the log:

- From the left sidebar, choose **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under AI Search, click on the {% icon classes="fas fa-download" /%} icon.
- Select the duration to download the logs for. 

The logs contain a UID which is an anonymous identifier of the user. It can help understand the different questions a user has asked.

## Limitations of AI Search

- Prone to provide incorrect, misleading or incomplete answers.
- No analytics are collected yet.
- AI Search only works on [Next UI](/support-center/customising-visuals#next-ui).

## What data is sent to OpenAI?

When enabling AI search for a project, the entirety of the content that readers can access is sent to OpenAI. Whenever content is re-indexed, the new content would be sent to OpenAI.
