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

- [AI Agent](ai-agent.md): Ask for a change in a conversation and have it drafted across your pages, API references and changelog posts for you to review.
- [Self-Updating Docs](self-updating-docs.md): Attach your code repositories so the agent can check what your docs claim against what your code does, and draft the updates a pull request implies.
- [AI Writer](writing-documentation/ai-writer.md): Provides AI functions to manipulate text, including shortening, enhancing and grammar correction.
- [AI Assistant](writing-documentation/ai-search.md): Ask questions about the docs in natural language and receive GPT powered answers.
- [AI Commit Messages](ai-features/ai-commit-messages.md): Automatically annotate page histories.
- [AI SEO Helper](ai-features/ai-summarisation.md): Summarises pages to write a META description.
- [MCP Servers](ai-features/mcp-server.md): Connect AI applications with your docs, so readers can search them and editors can write them.
- [Feedback Spam Filter](feedback.md#feedback-spam-filter): Filters spam in feedback messages automatically.
- [Redact PII from Feedback](feedback.md#redact-pii-from-feedback): Redacts personal identifiable information from feedback messages automatically.

Read the linked sections to understand what information we send for each feature.

## AI Credits

AI credits pay for [AI Agent](ai-agent.md), including the pull request checks under [Self-Updating Docs](self-updating-docs.md). No other feature on this page spends them.

A plan with AI features includes a monthly allowance of credits, which renews with your billing period. How many depends on the plan; see [Pricing](https://developerhub.io/pricing). Credits belong to a project, so each of your projects has its own allowance.

Each message you send the agent spends credits from the balance. How many depends on the size of the job, so correcting a page costs less than restructuring a section.

You can see what a project has left in three places:

- The **AI Editor** window, in its top bar.
- This page, at the end of the row holding the **Agent** and **Readers** tabs.
- Project Settings → **Billing** → **Plan \& Usage**, under **AI credits**, which shows the full picture and when the allowance renews.

Admins are emailed once when a project drops to 20% of its allowance. You can turn that email off in [Account Settings](account-settings.md#email-notifications).

### Running out

With no credits left, the agent will not start a new run, and pull request checks stop until the allowance renews or you top up. A run already under way finishes what it can and keeps everything it has staged for you to review.

Everything else carries on as normal, including your published documentation and every other AI feature.

### Topping up

To buy more before your allowance renews, open Project Settings → **Billing** → **Plan \& Usage** and use **Top up** under **AI credits**. Bought credits sit on top of your monthly allowance, survive a plan change, and last 12 months. Your allowance is always spent first.

On an enterprise plan, credits are a term of your contract instead. [Contact Us](contact-us.md) and we will size them to your team.

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
