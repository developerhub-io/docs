---
type: page
title: Editor MCP Server
listed: true
description: 
index_title: Editor MCP Server
hidden: false
keywords: 
tags: ai
---

The **Editor MCP server** lets your team edit a project from an AI client. Connect Claude, Cursor, Codex, or any other MCP-compatible agent, and it can find your pages, read them, write them, publish them, and check them for broken links without you leaving the tool you are already working in.

This is the counterpart to the [Reader MCP Server](reader-mcp-server.md). That one exposes your published docs so an agent can search them; this one exposes the editor so an agent can change them.

{% callout type="warning" title="Admins only" %}
Only project admins can turn the Editor MCP server on or off.
{% /callout %}

## Enabling the Editor MCP server

- Open Project Settings → **AI Features**.
- Turn on **Editor MCP server**.
- Click **Save changes** in the top menu.

It can take up to 5 minutes for the change to take effect. Once the setting is saved on, the card expands to show the connection details for your AI client.

Turning the setting off again disconnects every client that was connected to the project.

## Connecting your AI client

The server is at `https://ai.developerhub.io/mcp` and uses the Streamable HTTP transport.

For Claude Code:

{% code %}
```bash
claude mcp add --transport http developerhub https://ai.developerhub.io/mcp
```
{% /code %}

For Cursor, Codex, and other clients that take a configuration file:

{% code %}
```json
{
  "mcpServers": {
    "developerhub": {
      "url": "https://ai.developerhub.io/mcp"
    }
  }
}
```
{% /code %}

### Signing in

The first time a client connects, it opens a browser page asking you to **Allow access**. The page names the client that is asking, the account you are about to grant access as, and the address approving sends the authorisation to. Only continue if you started the connection yourself from a client you trust.

There is no key to create or share out. Every editor connects with their own %product% account and the agent acts as that person, so it reaches only the projects they can already edit, and only those with the Editor MCP server turned on.

The connection lasts as long as your %product% login does. After that your client asks you to approve access again.

## What an agent can do

| Tool | What it does |
| --- | --- |
| `list_projects` | Lists the projects you can edit. Every other tool needs a project, so an agent starts here. |
| `list_versions` | Lists a project's versions. |
| `clone_version` | Copies a version, with its documentation and API references, into a new one. |
| `list_documentation_sections` | Lists the documentation sections in a version. |
| `list_api_references` | Lists the API references in a version. |
| `list_pages` | Lists the pages in a version, optionally filtered by title or slug. |
| `find_page_by_slug` | Resolves a page from its slug. |
| `find_text` | Finds exact text across every page in a version, drafts included. |
| `search_pages` | Runs a relevance search over the published pages in a version. |
| `get_page` | Reads a page's editable body as Markdoc. |
| `create_page` | Creates a page, optionally nested under an existing one. It starts unpublished. |
| `edit_page` | Changes a page's body, title, slug, or any combination of the three. |
| `publish_page` | Publishes a page's draft. |
| `delete_page` | Permanently deletes a page. |
| `edit_api_reference` | Replaces the draft OpenAPI spec of an [API reference](../../api-references.md). |
| `check_broken_links` | Checks a single page, or a whole version, for [broken links](../../writing-documentation/page-linking.md#listing-broken-links). |
| `get_markdoc_syntax` | Returns the Markdoc reference the agent writes against. |
| `list_audiences` | Lists the project's audiences, for [adaptive content](../../conditional-content.md). |
| `validate_markdoc` | Checks a body for content that would be silently dropped, without writing it. |

## Drafts, renames and deletions

Body edits are written to the page's **draft**, so nothing an agent writes is visible to readers until it is published, and publishing is a separate, explicit step. Two things work differently, and both are worth knowing before you point an agent at a live project:

- **Titles and slugs are not drafted.** A rename takes effect straight away, published pages included. Changing a slug changes the page's URL, so [check what links to it](../../writing-documentation/page-linking.md) first.
- **Deleting a page cannot be undone.** An agent has to pass the page's current slug back as confirmation, so it cannot delete a page it has not looked up, but once the deletion goes through the page is gone.

## Writing Markdoc

Page bodies are [Markdoc](../../github-sync/markdoc-format.md) in %product%'s own dialect, which is not interchangeable with generic Markdoc. An agent writing from general knowledge produces something that saves but is wrong: custom blocks decay into literal text, and links with no text disappear.

The server carries the answer with it. `get_markdoc_syntax` returns the dialect reference with a worked example of every block, and `validate_markdoc` reports what a body would lose before anything is written. When an agent edits your pages from a Git repository instead, the [Agent Skills](../../github-sync/write-markdoc-with-ai.md) teach it the same dialect.
