---
type: page
title: WebMCP
listed: true
description: 
index_title: WebMCP
hidden: false
keywords: webmcp, mcp, ai agents, browser
tags: ai
---

Every page of your published docs offers a set of tools to AI agents running in your reader's browser, through **WebMCP**. An agent can search your docs, read a page as Markdown and open a page for the reader, without being connected to an MCP server first.

There is nothing to set up. The tools are on for every project.

{% callout title="Browser support" %}
WebMCP is new. For now, only Chrome supports it, and only with its testing flag turned on. Your readers get the tools as browsers ship it, with nothing to change on your side.
{% /callout %}

## Tools Available

| Tool | What it does |
|---|---|
| `search_docs` | Searches your docs and returns the best matching pages, each with a short excerpt and its URL. |
| `read_page` | Returns a page as Markdown: the one the reader has open, or any page by its URL. On an API reference, it can read a single endpoint. |
| `get_site_overview` | Returns your [llms.txt](llms-txt.md): every page, grouped by section, with its URL. |
| `navigate_page` | Opens a page of your docs in the reader's tab. |

`read_page` and `get_site_overview` read your docs through [llms.txt](llms-txt.md), so they are only offered while **Enable llms.txt** is on under Project Settings → **AI** → **AI Agents \& MCP** → **Readers**.

## What an Agent Can See

An agent uses your reader's own access. On [private docs](../private-docs.md), or pages shown to some [audiences](../conditional-content.md) only, it reads exactly what that reader could already open, and nothing more.

Searches an agent runs are not counted in your [search analytics](../search-analytics.md).

## WebMCP and the Reader MCP Server

The [Reader MCP Server](mcp-server/reader-mcp-server.md) is for AI clients such as Cursor or VS Code, which connect to your docs at `/mcp`. WebMCP is for an agent working inside the browser, on the page your reader has open, so it needs no connection.
