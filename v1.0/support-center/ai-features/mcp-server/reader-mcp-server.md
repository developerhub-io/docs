---
type: page
title: Reader MCP Server
listed: true
description: 
index_title: Reader MCP Server
hidden: false
keywords: 
tags: ai
---

The **Reader MCP Server** lets your readers connect their own AI agent directly to your docs, so it can search them, find its way around them and read any page or API endpoint as Markdown.

The MCP integration lets agents access your docs via a standardised protocol endpoint under the `/mcp`  route of your docs URL, for example: `https://docs.example.com/mcp`.

When an MCP-compatible client or AI agent connects to this route, it can use the tools exposed by the MCP server to interact with your docs.

This server is read-only and covers your published docs. To let your own team write and publish pages from an AI client, see the [Editor MCP Server](editor-mcp-server.md).

## Tools Available

The tools available under the MCP server are:

- `search`: Searches your docs and returns the most relevant excerpts, each with the page it came from. With [AI Assistant](../../writing-documentation/ai-search.md) on, it takes natural-language questions; otherwise, it searches by keywords.
- `list_versions`: Lists your published versions with their slugs, and which one is the default.
- `list_sections`: Lists the documentation sections and API references of a version, with their slugs.
- `list_pages`: Lists the pages of a documentation section, nested as your sidebar shows them, each with its URL.
- `read_page`: Reads a documentation page as Markdown, by its URL.
- `list_endpoints`: Lists the endpoints of an API reference (method, path and summary), grouped by tag, each with its URL.
- `read_endpoint`: Reads one endpoint as Markdown, by its URL: its parameters, request body and responses, with the schemas they use.

Every tool works on your default version unless the agent names another. An API reference is read one endpoint at a time, never whole, so an agent lists the endpoints first and then reads the ones it needs.

The MCP server supports the Streamable HTTP transport.

{% callout title="Need another tool?" %}
If your readers' agents need something these tools do not cover, [contact us](../../contact-us.md) with the details.
{% /callout %}

## What an Agent Can See

An agent sees exactly what its reader can open: your published versions, documentation sections, API references and pages. On public docs, that is what an anonymous visitor sees. On [private docs](#private-docs), the reader signs in, so the agent also sees the pages for their [audiences](../../conditional-content.md). Anything else looks to the agent like a page that does not exist.

## Enabling MCP Server

The MCP server is available on every plan and does not need AI Assistant. To enable it:

- Open Project Settings → **AI** → **AI Agents \& MCP**, then the **Readers** tab.
- Under **MCP server**, turn on **MCP server**.
- Click **Save changes** in the top menu.

It will take up to 5 minutes for the change to occur.

The MCP server does not depend on [llms.txt](../llms-txt.md). It reads your pages as Markdown whether **Enable llms.txt** is on or off.

If the [AI Tools button](../ask-llm.md) is on, readers can connect Claude Code, Codex, VS Code, or Cursor to your docs from its **Connect your AI tool** menu item. The button itself needs llms.txt on.

## Private Docs

The MCP server works on [private docs](../../private-docs.md) too, whichever way your readers log in. Readers connect their AI app to the same `/mcp` route, and the first time, the app asks them to sign in:

1. Their browser opens your docs site, and they log in the way they usually do.
2. A **Connect your AI app** card names the app that is asking. They click **Allow access**.

The app then reads your docs as that reader. It keeps access while the reader stays signed in to your docs, for 30 days at most, and then asks them to sign in again. Anything that ends the reader's access ends the app's at once.

## Try out our MCP Server

You can test out our own MCP server before enabling it on your docs. For a quick test, click the arrow next to **Copy page** at the top of this page \> **Connect your AI tool**. Alternatively, you can do it manually. Let's take Cursor as the MCP client for an example:

- Launch **Cursor**.
- Under **Settings** \> **Cursor Settings**.
- Click on **Tools** in the sidebar.
- Click **New MCP Server**.
- In the file that was opened, enter the following:

```json
{
  "mcpServers": {
    "DeveloperHub Docs": {
      "url": "https://docs.developerhub.io/mcp"
    }
  }
}
```

- Save the file.
- Toggle the AI pane {% key key="⌘" /%} + {% key key="I" /%}.
- Ask the agent a question like "Search DeveloperHub docs for how to add an image", or "List the pages of the DeveloperHub Support Center, then read the one on callouts".

{% image url="https://uploads.developerhub.io/prod/02/7z38mrq35ibpdzkkv3cxcjrehb3rlgqdl98qymu45brpn8y10wtgt4sbcdyqayyl.png" /%}
