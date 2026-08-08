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
- A changelog or one of its posts is created, edited, or deleted.
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
├── changelogs/                    # changelogs, which belong to the project, not to a version
│   └── product-updates/           # a changelog: the folder name is its path
│       ├── _settings.yaml         # changelog settings
│       └── 4-august-2026.md       # a post: filename (minus .md) is the slug
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

- **developerhub.yaml** (repository root): the project `title` and `variables`. Everything else at the root (your `README`, `LICENSE`, `.gitignore`, and so on) is left untouched.
- **\{version\}/\_settings.yaml**: version settings, plus the order of documentation sections and references.
- **\{version\}/\{documentation\}/\_settings.yaml**: documentation settings.
- **\{version\}/\{documentation\}/\_nav.yaml**: the sidebar order, categories, labels, separators, external links, and any [icons](structuring-documentation/index-icons.md) for that documentation.
- **\{version\}/refs/**: API reference specs, one file per reference.
- **changelogs/**: your [changelogs](changelogs.md), one folder per changelog and one file per post. Changelogs belong to the project rather than to a version, so this sits beside the version folders (see [Changelogs](github-sync.md#changelogs)).
- **assets/**: images the sync has stored. In a page you can also reference an image by a relative path to a file you commit next to it.

Page content is written in [Markdoc](github-sync/markdoc-format.md); settings and navigation are YAML.

{% callout title="Full repository rules" %}
For the complete rules (how to add, move, nest, group, reorder, or hide pages, versions, and references; the exact settings keys; and the round-trip gotchas), use the `organize-docs-repo` [Agent Skill](github-sync/write-markdoc-with-ai.md), or read it on [GitHub](https://github.com/developerhub-io/dh-skills).
{% /callout %}

## Changelogs

[Changelogs](changelogs.md) sync alongside your pages, so you can write a release note in the repository and open a pull request for it like any other change.

Each changelog is a folder under `changelogs/`, named after its path (the segment readers see in its URL). Each post is a single file, and its filename without `.md` is the post's slug. A post's frontmatter carries three fields, followed by the body in [Markdoc](github-sync/markdoc-format.md):

{% code %}
```markup {% title="changelogs/product-updates/4-august-2026.md" %}
---
title: 4 August 2026
date: 2026-08-04
published: true
---

- {% badge type="success" text="New" /%} **Changelogs**: release notes now sync to your repository.
```
{% /code %}

- **title**: the post title.
- **date**: the date readers see and the one posts are sorted by. A plain date is enough; add a time (`2026-08-04 14:30:00`) to order several posts within the same day.
- **published**: whether the post is live. Leave it out and the post stays unpublished, so pushing a file never puts a post live by accident.

The changelog's own `_settings.yaml` takes `title`, `description`, and `published`. Its path is the folder name, so rename the folder to change it. A changelog with no posts is still valid; its `_settings.yaml` is what keeps it in the repository.

{% callout title="Reserved folder name" %}
`changelogs` at the base path is reserved, so a version cannot use it as a slug. If your project already syncs, your existing changelogs are committed to the repository on the next sync.
{% /callout %}

Two things differ from pages. Links in a post body use full site paths such as `/support-center/getting-started`, not the relative `.md` paths pages use. And posts have no draft state, so changelog files are not mirrored to a [draft branch](github-sync.md#draft-branch); edit them on your published branch.

## Editing with AI Agents

If you edit the repository with an AI coding agent (in your IDE or a docs-as-code pipeline), install the DeveloperHub [Agent Skills](github-sync/write-markdoc-with-ai.md) so it writes correct Markdoc and the correct repository structure.

In Claude Code, install them as a plugin, which is the one channel that updates itself:

{% code %}
```
/plugin marketplace add developerhub-io/dh-skills
/plugin install dh-skills@developerhub
```
{% /code %}

For Cursor, Codex, and other agents, use the `skills` CLI:

{% code %}
```bash
npx skills add developerhub-io/dh-skills
```
{% /code %}

The package ships two skills: `write-markdoc` for the [Markdoc](github-sync/markdoc-format.md) syntax inside a page, and `organize-docs-repo` for the repository layout (navigation, settings, images, references, and changelogs). Together they keep an agent's edits lossless, so they sync back without churn or lost content.

## Pull Request Checks

On repositories synced through the GitHub App, %product% checks every pull request whose base is your synced branch. The check is a read-only dry run of the sync: it reports what would happen and never writes anything.

- Broken relative links or images, and invalid settings, navigation, reference specs, or changelog post frontmatter, **fail** the check.
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

## When a Change Is Blocked

If a change arriving from the repository would remove most of your documentation, %product% refuses it instead of applying it. Nothing is deleted and nothing is changed. The run appears in the **Sync activity** feed as **Change blocked, nothing was removed**, with the reason, and the status chip at the top of the pane reads **Sync paused**.

A change is blocked when:

- `developerhub.yaml` is missing from the repository root, or the repository holds no documentation at all. This usually means the branch or repository was pointed somewhere unintended, or the initial export was reverted.
- The change would remove every version.
- The change would remove most of your pages.

Sync stays paused on that commit until the repository is put right, so a later push cannot slip past while the problem is still there. There is nothing to clear on the %product% side: push a fix to the synced branch and the next sync runs normally. If the removal really was intended, [contact support](contact-us.md) and we will let that specific commit through.

## Disconnecting GitHub Sync

To stop syncing, open the **Git Sync** pane and use **Disconnect GitHub** (under Danger zone). Your repository files are left in place; only the connection is removed.

You can also remove the `DeveloperHub - Sync` application from your GitHub settings (under your personal or organisation GitHub application settings). Once it is removed, the connection is freed on %product%'s side automatically.
