---
type: page
title: MCP Servers
listed: true
description: 
index_title: MCP Servers
hidden: false
keywords: 
tags: ai
---

%product% integrates with **MCP (Model Context Protocol)**, the standard that lets AI applications connect to an external system and use the tools it exposes. There are two MCP servers, and they serve different people.

{% cards %}
{% card title="Reader MCP Server" text="Let readers search your published docs from their own AI client" link="mcp-server/reader-mcp-server.md" /%}
{% card title="Editor MCP Server" text="Let your team write and publish your docs from an AI client" link="mcp-server/editor-mcp-server.md" /%}
{% /cards %}

## Which one you need

The [Reader MCP Server](mcp-server/reader-mcp-server.md) runs on your documentation site, at the `/mcp` route of your docs URL. It is read-only and covers your published docs: an agent connected to it can search them and quote them back, which is what you want when your customers are building against your product with an AI assistant open.

The [Editor MCP Server](mcp-server/editor-mcp-server.md) is for your own team. It connects an AI client to the editor, so an agent can find, write, publish and delete pages in your project. Each editor connects with their own %product% account and the agent acts as that person, so it reaches only the projects they can already edit.

Both are turned on per project under Project Settings → **AI** → **AI Features**, the reader server on the **Readers** tab and the editor server on the **Agent** tab, and both use the Streamable HTTP transport.
