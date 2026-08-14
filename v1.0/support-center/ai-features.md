---
type: page
title: AI Features
listed: true
description: 
index_title: AI Features
hidden: false
keywords: 
tags: ai
---

We offer a range of AI features designed to streamline your tasks and enhance efficiency.

By default, all features are disabled and require activation by an admin. You will find them under Project Settings → **AI** → **AI Features**, split across an **Agent** tab for the features your team uses and a **Readers** tab for what your readers' AI tools can do with your documentation.

The features are:

- [AI Agent](/support-center/ai-agent): Ask for a change in a conversation and have it drafted across your pages, API references and changelog posts for you to review.
- [Self-Updating Docs](/support-center/self-updating-docs): Attach your code repositories so the agent can check what your docs claim against what your code does, and draft the updates a pull request implies.
- [AI Writer](writing-documentation/ai-writer.md): Provides AI functions to manipulate text, including shortening, enhancing and grammar correction.
- [AI Assistant](using-search/ai-search.md): Ask questions about the docs in natural language and receive GPT powered answers.
- [AI Commit Messages](ai-features/ai-commit-messages.md): Automatically annotate page histories.
- [AI SEO Helper](ai-features/ai-summarisation.md): Summarises pages to write a META description.
- [MCP Servers](ai-features/mcp-server.md): Connect AI applications with your docs, so readers can search them and editors can write them.
- [Feedback Spam Filter](feedback.md#feedback-spam-filter): Filters spam in feedback messages automatically.
- [Redact PII from Feedback](feedback.md#redact-pii-from-feedback): Redacts personal identifiable information from feedback messages automatically.

Read the linked sections to understand what information we send for each feature.

## Which models we use

The documentation agent, and the pull request checks that run on it, use the model an admin picks for the project under Project Settings → **AI** → **AI Features** → **Agent** → **Agent model**. Each option shows the provider that serves it and the region it runs in, so you can rule out a jurisdiction if you need to, and **Auto** follows our current recommendation.

Those runs are served through OpenRouter, and only providers with zero data retention are used. Your content is never kept and never used to train a model.

Our other AI features, including AI Writer, AI commit messages, AI Assistant and the feedback filters, use OpenAI's GPT models.

## Terms \& Conditions

For the features that use OpenAI, quoting from [OpenAI's Data Controls](https://developers.openai.com/api/docs/guides/your-data):

"Your data is your data. As of March 1, 2023, data sent to the OpenAI API is not used to train or improve OpenAI models".

However:

"OpenAI retains API data for 30 days for abuse and misuse monitoring purposes. A limited number of authorized OpenAI employees, as well as specialized third-party contractors that are subject to confidentiality and security obligations, can access this data solely to investigate and verify suspected abuse."

By using any AI services or features that %product% provides, you accept the transfer of the relevant data to the provider serving that feature.
