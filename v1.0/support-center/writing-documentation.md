---
type: page
title: Writing Documentation
listed: true
description: 
index_title: Writing Documentation
hidden: false
keywords: 
tags: 
---

Writing documentation on %product% cannot be any easier. In your editor pages, click anywhere on the text in your documentation and start writing down. You can even use [the AI Writer](writing-documentation/ai-writer.md) to help you craft the best content. Everything in the editor will be shown to you just as your readers, so there is no split view and no separate preview to keep in sync.

{% image url="../../assets/a4ee5d20d8356d9e2a15d522065de28186d599c9.png" /%}

## Ways to write

The editor is one of several ways to get content into your docs. They all write to the same pages, so your team can pick whichever suits them and mix them freely.

- **In the editor.** Write in place in your browser, exactly as your readers will see it. That is what the rest of this page covers.
- [**As code, in Git**](github-sync.md)**.** Sync a GitHub repository two ways and write your pages as files, so a change can go through a pull request before it reaches your readers.
- [**From an AI client**](ai-features/mcp-server/editor-mcp-server.md)**.** Connect Claude, Cursor, or another MCP client to your project and let it find, write and publish pages for you.
- [**With the AI Agent**](ai-agent.md)**.** Describe what you want in the editor's chat panel, then review the edits it suggests before applying them.

## Editing

The editor works in place: what you see is what your readers get. Three things are worth knowing to get around quickly.

- **Add a block.** Type {% key key="/" /%} on an empty line to open the insert menu, then search for and pick the block you want (a callout, image, table, code block and more). See [blocks](writing-documentation/blocks.md) for the full list.
- **Format text.** Select any text to bring up the formatting toolbar. From there you can make text **bold**, *italic*, underlined, struck through or `inline code`, turn the block into a heading or list with **Turn into**, add a [link](writing-documentation/page-linking.md), or leave a [comment](comments.md).
- **Move or change a block.** Hover over a block and use the drag handle to its left to move it, or open the handle's menu for more options such as deleting the block.

You can also drop in [links](writing-documentation/page-linking.md), [variables](variables.md) and [glossary terms](glossary.md) inline by typing `@`, `%` or `<`.

## Page Sections

Pages must have a **title** and **content**.

### Title

The title of the page will be visible in:

1. The index of the documentation.
2. The title of the browser tab.
3. The URL of the page.

So choose the title carefully to be meaningful to your readers.

### Content

The content of the page can consist of text, [tables](tables.md), [images](images.md), [links](writing-documentation/page-linking.md), [code blocks](code-blocks.md), lists, [information boxes](callouts.md), and much more! Have a look at [blocks](writing-documentation/blocks.md) to find all the content that we natively support.

## Saving

To save a page, hit the Save Draft button {% icon classes="fas fa-cloud-upload-alt" /%} at the bottom right. Your edits will be saved in [draft mode](writing-documentation/draft-mode.md) until you publish them. Every edit you make is saved in the [page history](page-history.md).

When you are ready to publish the changes to your readers, click the Publish button {% icon classes="fas fa-forward" /%}.

## Spell Check

Your browser spell checker is doing its job right away.
