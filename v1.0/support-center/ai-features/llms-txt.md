---
type: page
title: llms.txt
listed: true
description: 
index_title: llms.txt
hidden: false
keywords: 
tags: ai
---

{% callout type="warning" title="Beta" %}
This is a beta feature. Your [feedback](../contact-us.md) is appreciated.
{% /callout %}

The file named `llms.txt`, located at the base of your project path, is integral for enabling large language models (LLMs) to effectively process and understand your documentation. It's the equivalent of your docs but its intended audience is a computer rather than a human. `llms.txt` is generated using a standard format from your docs.

## Enabling llms.txt

`llms.txt` support is enabled by default for new projects. To enable `llms.txt`:

- Open Project Settings → **AI** → **AI Agents \& MCP**, then the **Readers** tab.
- Under **LLM friendliness**, turn on **Enable llms.txt**.
- Click **Save changes** in the top menu.

`llms.txt` file can be found at the base of your project.

For projects without a basepath: `https://<project-url>/llms.txt`.

For projects with a basepath: `https://<project-url>/<basepath>/llms.txt`.

{% callout title="Info" %}
`llms.txt` is updated every 6 hours
{% /callout %}

## Markdown for LLMs

When llms.txt is enabled, pages are also readable in markdown format if `.md` is added to the end of a URL. For example, if you visit this page with `.md` added to the end of its URL, then you can read its markdown equivalent:

[https://docs.developerhub.io/support-center/llms-txt.md](https://docs.developerhub.io/support-center/llms-txt.md)

An AI assistant that fetches one of your pages because someone asked it about your docs is given the markdown at the page's own URL, without the `.md`. Assistants such as ChatGPT, Claude, and Perplexity read your docs this way; crawlers that index the web for search or training still get the page itself.

A documentation section's URL answers with a list of the pages inside it, so an assistant can find its way around before reading anything.

## Limitations of llms.txt support

- We only support `llms.txt` for now. `llms-full.txt` is not supported yet.
