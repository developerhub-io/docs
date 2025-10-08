---
type: page
title: MCP Server
listed: true
slug: mcp-server
description: 
index_title: MCP Server
hidden: 
keywords: 
tags: 
---

%product% now integrates with **MCP (Model Context Protocol)** servers, allowing AI agents to connect directly to your docs and perform contextual actions like intelligent search.

The MCP integration lets agents access your docs via a standardised protocol endpoint under the `/mcp`  route of your docs URL, for example: `https://docs.example.com/mcp`.

When an MCP-compatible client or AI agent connects to this route, it can use the tools exposed by the MCP server to interact with your docs.

## Tools Available

The tools available under the MCP server are:

- `search`: Runs an AI search over your docs.

The MCP server supports the Streamable HTTP transport.

{% callout type="info" title="More tools?" %}
If you need more tools, [contact us](/support-center/contact-us) with the details!
{% /callout %}

## Enabling MCP Server

To enable the MCP server:

- From **Project Settings** {% icon classes="fas fa-layer-group" /%}, scroll down to AI Features.
- Check **Enable MCP Server**.

It will take up to 5 minutes for the change to occur.

## Limitations

MCP server is only available for public projects. [Contact us](/support-center/contact-us) if you'd like to add it for a private project.

## Try out our MCP Server

You can test out our own MCP server before enabling it on your docs. Let's take Cursor as the MCP client for an example:

- Launch **Cursor**.
- Under **Settings** &gt; **Cursor Settings**.
- Click on **Tools** in the sidebar.
- Click **New MCP Server**.
- In the file that was opened, enter the following:

{% code %}
{% tab language="json" %}
{
  "mcpServers": {
    "DeveloperHub Docs": {
      "url": "https://docs.developerhub.io/mcp"
    }
  }
}
{% /tab %}
{% /code %}

- Save the file.
- Toggle the AI pane {% key key="⌘" /%} + {% key key="I" /%}.
- Ask the agent a question like "Search DeveloperHub docs for how to add an image".

{% image url="https://uploads.developerhub.io/prod/02/7z38mrq35ibpdzkkv3cxcjrehb3rlgqdl98qymu45brpn8y10wtgt4sbcdyqayyl.png" mode="responsive" height="943" width="1398" %}
{% /image %}