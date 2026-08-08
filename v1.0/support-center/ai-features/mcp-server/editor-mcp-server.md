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

The same install steps are in your own [Account Settings](../../account-settings.md) → **Integrations** → **AI clients**.

### Signing in

The first time a client connects, it opens a browser page asking you to **Allow access**. The page names the client that is asking, the account you are about to grant access as, and the address approving sends the authorisation to. Only continue if you started the connection yourself from a client you trust.

There is no key to create or share out. Every editor connects with their own %product% account and the agent acts as that person, so it reaches only the projects they can already edit, and only those with the Editor MCP server turned on.

The connection lasts as long as your %product% login does. After that your client asks you to approve access again.

## What an agent can do

{% table %}
{% row %}
{% cell header=true colwidth=[273] %}
Tool
{% /cell %}
{% cell header=true %}
What it does
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`list_projects`
{% /cell %}
{% cell %}
Lists the projects you can edit. Every other tool needs a project, so an agent starts here.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`list_versions`
{% /cell %}
{% cell %}
Lists a project's versions.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`clone_version`
{% /cell %}
{% cell %}
Copies a version, with its documentation and API references, into a new one.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`list_documentation_sections`
{% /cell %}
{% cell %}
Lists the documentation sections in a version.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`list_api_references`
{% /cell %}
{% cell %}
Lists the API references in a version.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`list_pages`
{% /cell %}
{% cell %}
Lists the pages in a version, optionally filtered by title or slug.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`find_page_by_slug`
{% /cell %}
{% cell %}
Resolves a page from its slug.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`find_text`
{% /cell %}
{% cell %}
Finds exact text across every page in a version, drafts included.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`search_pages`
{% /cell %}
{% cell %}
Runs a relevance search over the published pages in a version.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`get_page`
{% /cell %}
{% cell %}
Reads a page's editable body as Markdoc.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`create_page`
{% /cell %}
{% cell %}
Creates a page, optionally nested under an existing one. It starts unpublished.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`edit_page`
{% /cell %}
{% cell %}
Changes a page's body, title, slug, or any combination of the three.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`publish_page`
{% /cell %}
{% cell %}
Publishes a page's draft.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`delete_page`
{% /cell %}
{% cell %}
Permanently deletes a page.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`edit_api_reference`
{% /cell %}
{% cell %}
Replaces the draft OpenAPI spec of an [API reference](../../api-references.md).
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`check_broken_links`
{% /cell %}
{% cell %}
Checks a single page, or a whole version, for [broken links](../../writing-documentation/page-linking.md#listing-broken-links).
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`get_markdoc_syntax`
{% /cell %}
{% cell %}
Returns the Markdoc reference the agent writes against.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`list_audiences`
{% /cell %}
{% cell %}
Lists the project's audiences, for [adaptive content](../../conditional-content.md).
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`validate_markdoc`
{% /cell %}
{% cell %}
Checks a body for content that would be silently dropped, without writing it.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`get_search_analytics`
{% /cell %}
{% cell %}
Reads what readers [search for](../../search-analytics.md) in your published docs.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`get_project_feedback`
{% /cell %}
{% cell %}
Reads the [feedback](../../feedback.md) across a project: the totals, the best and worst rated pages, and recent comments.
{% /cell %}
{% /row %}
{% row %}
{% cell colwidth=[273] %}
`get_page_feedback`
{% /cell %}
{% cell %}
Reads the ratings and comments on a single page.
{% /cell %}
{% /row %}
{% /table %}

## Drafts, renames and deletions

Body edits are written to the page's **draft**, so nothing an agent writes is visible to readers until it is published, and publishing is a separate, explicit step. Two things work differently, and both are worth knowing before you point an agent at a live project:

- **Titles and slugs are not drafted.** A rename takes effect straight away, published pages included. Changing a slug changes the page's URL, so [check what links to it](../../writing-documentation/page-linking.md) first.
- **Deleting a page cannot be undone.** An agent has to pass the page's current slug back as confirmation, so it cannot delete a page it has not looked up, but once the deletion goes through the page is gone.

## Writing Markdoc

Page bodies are [Markdoc](../../github-sync/markdoc-format.md) in %product%'s own dialect, which is not interchangeable with generic Markdoc. An agent writing from general knowledge produces something that saves but is wrong: custom blocks decay into literal text, and links with no text disappear.

The server carries the answer with it. `get_markdoc_syntax` returns the dialect reference with a worked example of every block, and `validate_markdoc` reports what a body would lose before anything is written. When an agent edits your pages from a Git repository instead, the [Agent Skills](../../github-sync/write-markdoc-with-ai.md) teach it the same dialect.

## Analytics and feedback

Three tools read what your readers did rather than what your pages say, so you can ask an agent what to write next as well as ask it to write.

`get_search_analytics` returns what readers [searched for](../../search-analytics.md), defaulting to the terms that found nothing, which is the quickest way to spot a topic you have not covered. `get_project_feedback` and `get_page_feedback` return the ratings and comments readers left, across a project or on one page. Ratings with no comment written on them are left out by default, since the totals already count them.
