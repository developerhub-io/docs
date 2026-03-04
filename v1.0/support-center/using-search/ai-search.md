---
type: page
title: AI Assistant
listed: true
slug: ai-search
description: 
index_title: AI Assistant
hidden: 
keywords: 
tags: ai
---

An intelligent assistant that helps readers find answers through natural conversation. This feature uses OpenAI GPT models to provide contextual answers about your documentation and API endpoints.

Formerly called AI Search.

{% image url="asset:phevav8uo2iw" mode="responsive" height="831" width="1402" %}
{% /image %}

## AI Assistant Features

AI Assistant allows the readers to ask a questions about the docs and API endpoints, delivering GPT-powered responses. Features of AI Assistant:

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

## Enabling AI Assistant

To enable/disable AI Assistant:

- From the left sidebar, choose **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under AI Features, check or uncheck **Enable AI Search**.

Once AI Assistant is enabled, it might take a couple of minutes until it is useable.

## Search Update Frequency

New or deleted content would be effectively available within 30 minutes for AI Assistant.

## Validating Responses

To validate responses provided by AI Assistant, a log of all questions and answers can be downloaded.

To download the log:

- From the left sidebar, choose **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under AI Search, click on the {% icon classes="fas fa-download" /%} icon.
- Select the duration to download the logs for.

The logs contain a UID which is an anonymous identifier of the user. It can help understand the different questions a user has asked.

## Limitations of AI Assistant

- Prone to provide incorrect, misleading or incomplete answers.
- No analytics are collected yet.
- AI Assistant only works on [Next UI](/support-center/customising-visuals#next-ui).

## What Data Is Sent to the LLM?

When enabling AI Assistant for a project, the entirety of the content that readers can access is sent to the LLM. Whenever content is re-indexed, the new content would be sent to the LLM.