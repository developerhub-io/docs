---
type: page
title: Writing Markdoc with AI Agents
listed: true
description: 
index_title: Writing Markdoc with AI Agents
hidden: false
keywords: 
tags: 
---

%product% pages are authored in [Markdoc](markdoc-format.md), a superset of Markdown with a set of typed custom tags. When you edit pages with an AI coding agent (in your IDE, a [GitHub-synced](../github-sync.md) repository, or a docs-as-code pipeline), the agent needs to emit %product%'s exact Markdoc dialect. Emit a non-canonical shape and the edit churns on the first save, or silently drops content.

`@developerhub/dh-skills` is an open-source set of [Agent Skills](https://github.com/developerhub-io/dh-skills) that teach your agent that dialect and the repository structure %product% expects, so the pages it writes round-trip cleanly. They can also move your existing docs into %product% from another tool.

{% callout title="On GitHub" %}
The package is public and maintained by %product%: [github.com/developerhub-io/dh-skills](https://github.com/developerhub-io/dh-skills). It is released under the MIT licence.
{% /callout %}

## What it is

The package ships three skills:

- **write-markdoc** documents every %product% block and inline tag with its exact syntax, attributes, defaults, allowed values, and the round-trip rules that keep an edit lossless.
- **organize-docs-repo** covers the repository layout: where each file goes, the navigation and settings files, images, API references, synced blocks, changelogs, and your site's look (logo, favicon, colours, and custom CSS), and how to add, move, nest, group, reorder, or hide pages without breaking the sync.
- **migrate-docs** moves your docs from another tool, such as Docusaurus, MkDocs, Sphinx, GitBook, Mintlify, or ReadMe, into a folder you import with [GitHub Sync](../github-sync.md). See [Migrating from Another Tool](#migrating-from-another-tool).

They use the portable Agent Skills format (Markdown with YAML frontmatter), so they work across Claude Code, Cursor, Codex, and other compatible agents.

## When to use it

Reach for it whenever an agent, rather than the editor, is writing your pages:

- Editing pages in a [GitHub Sync](../github-sync.md) repository or any docs-as-code workflow.
- Any task where you want the agent to produce correct, lossless Markdoc the first time.
- Moving your docs to %product% from another tool.

The in-product editor already knows the format, so this skill is for agents working on your pages from outside %product%.

## Installing the skill

### Claude Code

The repository doubles as a Claude Code plugin marketplace. This is the only install that keeps itself current as the format evolves:

```
/plugin marketplace add developerhub-io/dh-skills
/plugin install dh-skills@developerhub
```

The skills arrive namespaced, as `dh-skills:write-markdoc`, `dh-skills:organize-docs-repo`, and `dh-skills:migrate-docs`.

Third-party marketplaces do not update themselves until you allow it, so turn that on once: run `/plugin`, open the **Marketplaces** tab, select **developerhub**, and choose **Enable auto-update**. Claude Code then refreshes the plugin in the background shortly after a session starts.

### Cursor, Codex, and other agents

Use the [skills CLI](https://www.npmjs.com/package/skills), which adds the skills to your agent's skills directory:

{% code %}
```bash
npx skills add developerhub-io/dh-skills
```
{% /code %}

This copies the files in, so run `npx skills update` when you want a newer release.

Alternatively, copy the folders under `skills/` from the repository into your agent's skills directory yourself (`.claude/skills/`, `.cursor/skills/`, and so on). Copy all three together, since `migrate-docs` relies on the other two.

The package is also on npm, for anyone who prefers to vendor the files as a dependency:

{% code %}
```bash
npm install @developerhub/dh-skills
```
{% /code %}

## Using it

Once installed, your agent picks the skills up automatically when a task involves your %product% docs: writing a callout, code block, table, image, or tabs; or changing structure, such as adding, moving, or reordering pages. They give the agent the canonical shape for each tag and the correct file layout, so its changes import cleanly and do not churn or drop content on the next save.

For the reference `write-markdoc` is built on, see [Markdoc Format](markdoc-format.md), which lists every block with an example.

## Migrating from Another Tool

Ask your agent to move your docs to %product%, and point it at them: a folder or repository, an export, or the live site if there is nothing else. It asks how you want your content structured, shows you the plan, and converts a few pages for you to check before it does the rest. Your writing is kept as it is.

The result is a folder ready for [GitHub Sync](../github-sync.md), with a report of the migration and a list of redirects from your old URLs. Push the folder to a GitHub repository and [set up GitHub Sync](../github-sync.md#setting-up-github-sync) with **First sync** set to **Import**. When you point your domain at %product%, paste the redirects into [URL Redirects](../hosting/url-redirects.md) so old links keep working.

## Feedback

Spotted an error, or want a block documented differently? [Open an issue](https://github.com/developerhub-io/dh-skills/issues) on the repository.
