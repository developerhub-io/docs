---
type: page
title: GitHub Sync
listed: true
description: 
index_title: GitHub Sync
hidden: false
keywords: 
tags: 
---

{% synced id="beta-feature" /%}

With %product% you can set up two-way sync with a GitHub repository. This lets you:

- Write your docs in %product% and keep a permanent copy in GitHub.
- Edit your docs in GitHub if your team prefers working in a local text editor, and have those changes reflect in %product% on push.
- Let readers suggest edits from GitHub, using GitHub's own editing and comment tools.
- Add your own GitHub workflow on top:
  - Review changes through pull requests.
  - Keep unpublished drafts on a separate branch.
  - Run GitHub Actions to lint or transform docs before they sync.

{% image url="https://uploads.developerhub.io/prod/02/5s6oz6b4qimfnm8uotra4tb1jzfn44wbrph802xb406g2q9e79lh4xaulqpbpe2p.jpg" /%}

## Setting up GitHub Sync

Set-up happens on both the GitHub side and the %product% side.

1. Create the repository you want to sync with, and make sure it has at least one commit (so it has a branch). An initial commit adding a `README` is enough.
2. In %product%, open Project Settings → **Integrations**.
3. Click **Connect** next to GitHub, then complete the authorisation on GitHub and grant access to the repositories you want to sync.

{% callout title="Multiple Projects" %}
If you have multiple projects, choose all the repositories you want to sync with.
{% /callout %}

You are taken back to %product% and land on the **Git Sync** settings pane (Project Settings → **Git Sync**). This is where you configure and monitor the sync from now on. Set:

- **Repository**: pick from the repositories the DeveloperHub GitHub App can access.
- **Branch**: the branch %product% commits to and pulls from.
- **Base path** (optional): for monorepos, the directory your docs live in (for example `docs/files`). Leave it empty to sync from the repository root.
- **First sync**: the direction of the very first sync. Choose **Export** to commit your existing %product% pages to the repository, or **Import** to bring the repository's files into %product%.
- **Reader edits**: turn on **Allow readers to suggest edits on GitHub** to show an "Edit on GitHub" link on every page.
- **Draft branch** (optional): mirror unpublished drafts to a separate branch (see [Draft branch](github-sync.md#draft-branch)).

Click **Start sync** to run the first sync. It can take a few minutes.

{% callout type="warning" title="Warning" %}
On an **Export** first sync, any repository files at the same paths as the exported files are overwritten.
{% /callout %}

{% callout title="Changing the base path" %}
Changing the base path re-scopes which part of the repository is mirrored, so %product% resets the sync state and runs the initial sync again.
{% /callout %}

## What Gets Synced

All published pages are synced. Pages that are still in draft and have never been published are not, unless you enable a [draft branch](github-sync.md#draft-branch).

%product% commits to the repository whenever:

- A published page's content changes (whether the page is listed or not).
- A page's settings change.
- A page is created, moved, renamed, or deleted.
- A documentation section is created, its settings change, or it is deleted.
- A version is created, its settings change, or it is deleted.
- The navigation order or grouping changes.
- An API reference is added or updated.
- Project settings (the title and variables) change.

Whenever a matching file is created or updated in the repository, the corresponding content or settings are updated in %product%.

{% callout title="Sync Error Notifications" %}
If an error occurs while syncing changes from GitHub to %product%, we email the person who pushed the commit.
{% /callout %}

## Repository Layout

The core idea is that **the path is the structure, and the filename is the slug**. A page's folder location sets its version, documentation section, and parent pages; its filename (without `.md`) is its URL slug. Ordering and grouping live in `_nav.yaml`, not in the folder layout.

From the base path, the repository is laid out like this:

{% code %}
```none
.
├── developerhub.yaml              # project settings: title and variables
├── assets/                        # images the sync has stored, addressed by content
│   └── 01f321...175.png
└── v1.0/                          # a version: the folder name is the version slug
    ├── _settings.yaml             # version settings, plus doc and reference order
    ├── refs/                      # API reference specs
    │   └── api.yaml               # the spec file; its name is the reference slug
    └── support-center/            # a documentation section: folder name is the slug
        ├── _settings.yaml         # documentation settings
        ├── _nav.yaml              # sidebar order, categories, labels, links
        ├── getting-started.md     # a page: filename (minus .md) is the slug
        ├── writing-documentation.md
        └── writing-documentation/ # a parent page's children live in a folder named after it
            └── formatting-text.md
```
{% /code %}

- **`developerhub.yaml`** (repository root): the project `title` and `variables`. Everything else at the root (your `README`, `LICENSE`, `.gitignore`, and so on) is left untouched.
- **`{version}/_settings.yaml`**: version settings, plus the order of documentation sections and references.
- **`{version}/{documentation}/_settings.yaml`**: documentation settings.
- **`{version}/{documentation}/_nav.yaml`**: the sidebar order, categories, labels, separators, and external links for that documentation.
- **`{version}/refs/`**: API reference specs, one file per reference.
- **`assets/`**: images the sync has stored. In a page you can also reference an image by a relative path to a file you commit next to it.

Page content is written in [Markdoc](github-sync/markdoc-format.md); settings and navigation are YAML.

{% callout title="Full repository rules" %}
For the complete rules (how to add, move, nest, group, reorder, or hide pages, versions, and references; the exact settings keys; and the round-trip gotchas), use the `organize-docs-repo` [Agent Skill](github-sync/write-markdoc-with-ai.md), or read it on [GitHub](https://github.com/developerhub-io/dh-skills).
{% /callout %}

## Editing with AI Agents

If you edit the repository with an AI coding agent (in your IDE or a docs-as-code pipeline), install the DeveloperHub [Agent Skills](github-sync/write-markdoc-with-ai.md) so it writes correct Markdoc and the correct repository structure:

{% code %}
```bash
npx skills add developerhub-io/dh-skills
```
{% /code %}

The package ships two skills: `write-markdoc` for the [Markdoc](github-sync/markdoc-format.md) syntax inside a page, and `organize-docs-repo` for the repository layout (navigation, settings, images, and references). Together they keep an agent's edits lossless, so they sync back without churn or lost content.

## Pull Request Checks

On repositories synced through the GitHub App, %product% checks every pull request whose base is your synced branch. The check is a read-only dry run of the sync: it reports what would happen and never writes anything.

- Broken relative links or images, and invalid settings, navigation, or reference specs, **fail** the check.
- Everything else is reported as a warning.

Three things keep it green:

- **Keep a move and a content rewrite in separate commits.** Doing both at once can defeat rename pairing, so the page would be treated as a delete plus a new page, and its history and comments would not follow.
- **The link scan only covers changed files.** Moving or deleting a page does not flag links to it from pages you did not touch, so check those yourself.
- **References and documentation sections share one slug namespace per version**, so a reference cannot take a documentation section's slug, or vice versa.

## Draft Branch

By default only published pages sync, and they sync to the branch you chose during set-up. You can optionally mirror unpublished draft edits to a separate branch, so writers and Git users collaborate on drafts before they go live.

In the **Git Sync** pane, turn on **Sync draft edits to a branch** and set a **Draft branch name** (the default is `developerhub-drafts`).

The draft branch is **body-only**: it carries page content, not structure. Structural work (adding, moving, and renaming pages, navigation, and settings, including page frontmatter) belongs on the published branch. A structural change made on the draft branch is deferred, not applied.

## Letting Readers Edit on GitHub

Turn on **Allow readers to suggest edits on GitHub** in the **Git Sync** pane to show an **Edit on GitHub** link on every page. The link opens the page's source file on your synced branch, where a reader can propose a change through GitHub's normal editing and pull request flow.

## Page History and Sync Activity

When an edit arrives from GitHub, the page's [edit history](page-history.md) records the commit message and links the commit's SHA, so you can open the exact commit on GitHub.

The **Git Sync** pane also has a **Sync activity** feed showing recent reconcile runs: each run's direction (**DeveloperHub → Repo** or **Repo → DeveloperHub**), what changed (for example "3 pages" or "1 API reference"), its commit, and when it ran. A status chip at the top shows whether the project is **In sync**, has **Changes pending**, or has not synced yet.

## Disconnecting GitHub Sync

To stop syncing, open the **Git Sync** pane and use **Disconnect GitHub** (under Danger zone). Your repository files are left in place; only the connection is removed.

You can also remove the `DeveloperHub - Sync` application from your GitHub settings (under your personal or organisation GitHub application settings). Once it is removed, the connection is freed on %product%'s side automatically.
