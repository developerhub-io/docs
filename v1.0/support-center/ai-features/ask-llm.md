---
type: page
title: AI Tools Button
listed: true
description: 
index_title: AI Tools Button
hidden: false
keywords: 
tags: ai
---

The AI Tools button sits next to a page title and reads **Copy page**. Clicking it copies the page as Markdown, ready to paste into any AI tool.

The arrow beside it opens a menu where readers can:

- **View as Markdown**: open the page's Markdown in a new tab.
- **Summarize this page**: ask the [AI Assistant](../writing-documentation/ai-search.md) for a summary. Shown when AI Assistant is on.
- **Ask ChatGPT about this page** or **Ask Claude about this page**: start a new chat that reads the page first.
- **Connect your AI tool**: add your docs to Claude Code, Codex, VS Code, or Cursor using the [Reader MCP Server](mcp-server/reader-mcp-server.md). Shown when the MCP server is on.

## Connecting an AI Tool

**Connect your AI tool** has a tab for each tool:

- **Claude Code** and **Codex**: copy the command and run it in a terminal.
- **VS Code** and **Cursor**: click **Add to VS Code** or **Add to Cursor**, then confirm in the app.

For any other MCP client, **Copy the MCP server URL** at the bottom copies the address to add by hand.

## Enabling the AI Tools button

The AI Tools button is enabled by default for new projects. To enable or disable it:

1. Open Project Settings → **AI** → **AI Agents \& MCP**, then the **Readers** tab.
2. Under **LLM friendliness**, ensure **Enable llms.txt** is on (required).
3. Toggle **Show AI tools button** on or off.
4. Click **Save changes** in the top menu.
