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

The **Reader MCP Server** lets your readers connect their own AI agent directly to your docs and perform contextual actions like intelligent search.

The MCP integration lets agents access your docs via a standardised protocol endpoint under the `/mcp`  route of your docs URL, for example: `https://docs.example.com/mcp`.

When an MCP-compatible client or AI agent connects to this route, it can use the tools exposed by the MCP server to interact with your docs.

This server is read-only and covers your published docs. To let your own team write and publish pages from an AI client, see the [Editor MCP Server](editor-mcp-server.md).

## Tools Available

The tools available under the MCP server are:

- `search`: Runs an AI search over your docs.

The MCP server supports the Streamable HTTP transport.

{% callout title="More tools?" %}
If you need more tools, [contact us](../../contact-us.md) with the details!
{% /callout %}

## Enabling MCP Server

To enable the MCP server:

- Open Project Settings → **AI Features**.
- Turn on **MCP server**.
- Click **Save changes** in the top menu.

It will take up to 5 minutes for the change to occur. If `AI Tools` button is enabled, the readers would be able to connect to Cursor and VS Code using the MCP server through the dropdown.

## Limitations

MCP server is only available for public projects. [Contact us](../../contact-us.md) if you'd like to add it for a private project.

## Try out our MCP Server

You can test out our own MCP server before enabling it on your docs. For a quick test, you can click the **AI Tools** button at the top of this page \> **Connect to Cursor**/**VS Code**. Alternatively, you can do it manually. Let's take Cursor as the MCP client for an example:

- Launch **Cursor**.
- Under **Settings** \> **Cursor Settings**.
- Click on **Tools** in the sidebar.
- Click **New MCP Server**.
- In the file that was opened, enter the following:

{% code %}
```json
{
  "mcpServers": {
    "DeveloperHub Docs": {
      "url": "https://docs.developerhub.io/mcp"
    }
  }
}
```
{% /code %}

- Save the file.
- Toggle the AI pane {% key key="⌘" /%} + {% key key="I" /%}.
- Ask the agent a question like "Search DeveloperHub docs for how to add an image".

{% image url="https://uploads.developerhub.io/prod/02/7z38mrq35ibpdzkkv3cxcjrehb3rlgqdl98qymu45brpn8y10wtgt4sbcdyqayyl.png" /%}
