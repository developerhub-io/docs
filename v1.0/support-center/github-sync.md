---
type: page
title: GitHub Sync
listed: true
slug: github-sync
description: 
index_title: GitHub Sync
hidden: 
keywords: 
tags: 
---

{% callout type="warning" title="Beta" %}
This is a beta feature. Your [feedback](/support-center/contact-us) is appreciated.
{% /callout %}

With %product% you can have two-way sync set up with GitHub. This enables you to:-

- Write your docs in %product% and have a permanent export in GitHub.
- Update your docs in GitHub if your team prefers using their local text editors to write docs, which would reflect to %product% on push.
- Enable readers to edit the docs from GitHub and even use GitHub's comment system.
- Do some fancy GitHub stuff:
    - Set up a pull request review system.
    - Keep drafted docs in a branch.
    - Use GitHub actions to modify or lint docs before pushing.

## Setting up GitHub Sync

The set up is needed from both GitHub side and %product% side. Follow the steps:

- From the left sidebar, open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}
- Under Integrations, click Connect next to GitHub.
- Complete the authorisation on GitHub and give access to the repositories with which you wish to sync.

{% callout type="info" title="Multiple Projects" %}
If you have multiple projects, choose all the repositories to sync with.
{% /callout %}

- You would be taken back to %product% to set up the integration.
- For the current project you are on, select the repository to sync with.
- Select the branch to sync with.
- If you wish for the docs to be synced under a different path (not root), enter it under base path.
- If you wish for the readers to see "Edit on GitHub" on every page, check "Allow readers to suggest edits on GitHub".
- Click Save.

On clicking Save, the initial sync process would start where all the files would be synced from %product% to GitHub. This could take minutes.

{% callout type="info" title="Info" %}
Initial sync occurs only from %product% to GitHub. No files from GitHub would be synced to %product% at this point.
{% /callout %}

{% callout type="warning" title="Warning" %}
Any files that match the same paths from the initial sync would be overwritten.
{% /callout %}

## What Gets Synced?

All pages are synced excluding pages that are still in draft mode and have not been published before.

Exactly, files would be synced to GitHub whenever a:

- Published page content is updated (regardless if page is listed or not),
- Page's settings are changed,
- Page is deleted,
- Documentation is created,
- Documentation's settings are changed,
- Documentation is deleted,
- Version is created,
- Version's settings are changed,
- Version is deleted,
- Version is imported (using Project Import),

Whenever a file is updated on GitHub, the corresponding contents or settings would be updated on %product%.

## File Formats

The files synced on GitHub are of two types:

- Contents: Such as page contents, formatted in [Markdoc](/support-center/markdoc-format).
- Settings: Such as documentation settings, formatted in YAML.

## File Structure

In the repository the files would be structured (from the basepath) as such:

- Folder for each version having the version slug as its name.
    - `settings.yaml` file containing the version settings.
    - Folder for each documentation section having the documentation slug as its name.
        - `settings.yaml` file containing the documentation settings.
        - File for each parent page having the page slug as its name with a `md` extension.
        - Folder for each parent page that has child pages, having the page slug as its name.
            - File for each child page having the page slug as its name with a `md` extension.

For example:

{% code %}
{% tab language="none" %}
.
├── README.md
├── v1.0
│   ├── docs
│   │   ├── getting-started.md
│   │   ├── check-api.md
│   │   └── settings.yaml
│   └── settings.yaml
└── v1.02
    ├── settings.yaml
    └── support-center
        ├── activity-log.md
        ├── ai-features.md
        ├── ai-summarisation.md
        ├── api-references
        │   ├── api-reference-faq.md
        │   ├── api-reference-settings.md
        │   ├── code-generation.md
        │   └── openapi-extensions.md
        ├── api-references.md
        ├── hosting
        │   ├── configure-dns.md
        │   ├── server-headers.md
        │   ├── url-redirects.md
        │   └── using-custom-domain.md
        ├── hosting.md
        └── writing-documentation.md
{% /tab %}
{% /code %}

## GitHub Sync in Beta

GitHub sync is a work-in-progress. At the moment, the following is not possible:

- Creating new pages, documentation sections or versions from GitHub.
- Ordering pages, documentation sections or version from GitHub.
- API references are not synced yet.
- Synced blocks are not synced yet.
- Project settings are not synced yet.

For any requirements, please [contact us](/support-center/contact-us).