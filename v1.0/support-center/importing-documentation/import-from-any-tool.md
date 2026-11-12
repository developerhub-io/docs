---
type: page
title: Import from Any Tool with AI
listed: true
description: Move your docs to DeveloperHub from Docusaurus, MkDocs, Sphinx, GitBook, or any other tool with the migrate-docs Agent Skill and your AI coding agent.
index_title: Import from Any Tool with AI
hidden: false
keywords: migrate,migration,docusaurus,mkdocs,sphinx,gitbook,vitepress,agent skill
tags: 
---

Moving from Docusaurus, MkDocs, Sphinx, GitBook, VitePress, or another tool? Your AI coding agent can do the move for you with the `migrate-docs` [Agent Skill](../github-sync/write-markdoc-with-ai.md). It converts your pages to %product% [Markdoc](../github-sync/markdoc-format.md), rebuilds your navigation, copies your images, and hands you a folder to import with [GitHub Sync](../github-sync.md).

Your writing is kept as it is. Only the syntax around it changes, and your original docs are never edited.

{% callout title="Coming from Mintlify or Zendesk?" %}
These have a built-in importer that needs no agent. See [Import from Mintlify](import-from-mintlify.md) and [Import from Zendesk](import-from-zendesk.md).
{% /callout %}

## Before You Start

- An AI coding agent that supports Agent Skills, such as Claude Code, Cursor, or Codex.
- Your docs in a form the agent can read: a folder on your computer, a Git repository, or an export from your current tool. If you have none of these, the agent can read your published site instead, though less structure comes across that way.
- A GitHub repository to import the result from. A new, empty private one is fine.

## Step 1: Install the Skills

The skill does not come with your agent, so install it first. It ships with two other skills it relies on, so install the whole package.

In **Claude Code**, run:

```
/plugin marketplace add developerhub-io/dh-skills
/plugin install dh-skills@developerhub
```

In **Cursor, Codex, or another agent**, run this in a terminal:

```bash
npx skills add developerhub-io/dh-skills
```

Then start a new session in your agent so it picks the skills up. For other ways to install, and how to keep the skills up to date, see [Writing Markdoc with AI Agents](../github-sync/write-markdoc-with-ai.md#installing-the-skill).

## Step 2: Ask Your Agent to Migrate

Open your agent and ask it to move your docs to %product%, pointing it at where they are:

```
Migrate my docs in ./website to DeveloperHub.
```

A repository link, an export file, or the address of your live site works too. In Claude Code, you can also start the skill directly with `/dh-skills:migrate-docs`.

Tell the agent where to put the result. If you do not, it suggests a new folder next to your docs.

## Step 3: Answer Its Questions

The agent looks through your docs first and reports what it found: how many pages, and the sections, versions, and languages they sit in. It then asks, in one go, about anything your current setup does not settle, such as:

- Which sections become separate documentation sections, and which stay as groups in one sidebar.
- Which versions and languages to bring across.
- Whether a blog or release notes become a [changelog](../changelogs.md).

Each question comes with a recommended answer, so you can reply "go with the defaults".

## Step 4: Check the First Pages

Before converting everything, the agent converts three to five representative pages and shows them to you. Check that they look right, and tell it what to change. It applies your feedback to the rest of the migration, not just those pages.

## Step 5: Review the Result

When it finishes, the agent checks its own output and hands you a folder containing:

- Your pages, navigation, and images in the layout GitHub Sync expects.
- `MIGRATION.md`, a report of what was migrated, the choices made, any pages whose address changed, and anything that needs your attention.
- `redirects.txt`, a list of redirects from your old page addresses to the new ones.

Read `MIGRATION.md` before you import. Anything that could not come across exactly is listed there with its file and line, so nothing is lost without you knowing.

## Step 6: Import with GitHub Sync

1. Push the folder to your GitHub repository. It can sit at the root or in a subfolder.
2. [Set up GitHub Sync](../github-sync.md#setting-up-github-sync) with that repository. If the folder is in a subfolder, enter it as the **Base path**.
3. Set **First sync** to **Import**, and click **Start sync**.
4. When it finishes, check the **Activity** tab of the **Docs Sync** pane for warnings.

{% callout type="warning" title="Sample content" %}
A new project starts with sample content: a documentation section with a Getting Started page, and a sample API reference. An import never deletes anything, so this stays next to your docs. Remove it once the import is done. Your agent's handoff notes tell you which parts are safe to delete.
{% /callout %}

## Step 7: Keep Your Old Links Working

When you point your domain at %product%, paste the contents of `redirects.txt` into [URL Redirects](../hosting/url-redirects.md). Links to your old pages, from search engines and other sites, then lead to the same pages on %product%.
