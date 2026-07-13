---
type: page
title: Writing Markdoc with AI Agents
listed: true
slug: write-markdoc-with-ai
description: 
index_title: Writing Markdoc with AI Agents
hidden: 
keywords: 
tags: 
---

%product% pages are authored in [Markdoc](/support-center/markdoc-format), a superset of Markdown with a set of typed custom tags. When you edit pages with an AI coding agent (in your IDE, a [GitHub-synced](/support-center/github-sync) repository, or a docs-as-code pipeline), the agent needs to emit %product%'s exact Markdoc dialect. Emit a non-canonical shape and the edit churns on the first save, or silently drops content.

`@developerhub/dh-skills` is an open-source [Agent Skill](https://github.com/developerhub-io/dh-skills) that teaches your agent that dialect, so the pages it writes round-trip cleanly.

{% callout type="info" title="On GitHub" %}
The package is public and maintained by %product%: [github.com/developerhub-io/dh-skills](https://github.com/developerhub-io/dh-skills). It is released under the MIT licence.
{% /callout %}

## What it is

The package ships the `write-markdoc` skill, which documents every %product% block and inline tag with its exact syntax, attributes, defaults, allowed values, and the round-trip rules that keep an edit lossless.

It uses the portable Agent Skills format (Markdown with YAML frontmatter), so it works across Claude Code, Cursor, Codex, and other compatible agents.

## When to use it

Reach for it whenever an agent, rather than the editor, is writing your pages:

- Editing pages in a [GitHub Sync](/support-center/github-sync) repository or any docs-as-code workflow.
- Driving the [CLI](/support-center/cli) or the API with an agent to create or update pages.
- Any task where you want the agent to produce correct, lossless Markdoc the first time.

The in-product editor already knows the format, so this skill is for agents working on your pages from outside %product%.

## Installing the skill

The quickest way is the [`skills` CLI](https://www.npmjs.com/package/skills), which adds the skill to your agent's skills directory:

{% code %}
```bash
npx skills add developerhub-io/dh-skills
```
{% /code %}

Alternatively, copy the `skills/write-markdoc` folder from the repository into your agent's skills directory yourself (`.claude/skills/`, `.cursor/skills/`, and so on).

The package is also on npm, for anyone who prefers to vendor the files as a dependency:

{% code %}
```bash
npm install @developerhub/dh-skills
```
{% /code %}

## Using it

Once the skill is installed, your agent picks it up automatically when a task involves creating or editing a %product% page: inserting a callout, code block, table, image, tabs, and so on. The skill gives the agent the canonical shape for each tag, so the page it writes imports cleanly and does not churn or drop content on the next save.

For the same reference the skill is built on, see [Markdoc Format](/support-center/markdoc-format), which lists every block with an example.

## Feedback

Spotted an error, or want a block documented differently? [Open an issue](https://github.com/developerhub-io/dh-skills/issues) on the repository.
