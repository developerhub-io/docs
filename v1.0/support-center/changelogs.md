---
type: page
title: Changelogs
listed: true
description: 
index_title: Changelogs
hidden: false
keywords: 
tags: 
---

Create a changelog for your docs using our Changelogs native feature.

Check out our own changelog: [Product Updates](/product-updates).

{% callout title="How is this different from writing a changelog on a page?" %}
Changelogs operate independently of specific versions, in contrast to pages. When a changelog is included within a page, it can quickly become outdated as soon as you clone a version and commence work on a new one.
{% /callout %}

## Creating a Changelog

To create a changelog:

- In the editor top navigation, open the scope picker and choose **Changelogs**.
- Click **Create new changelog**.
- Give it a title and click Create.

You can now change the path and description of the changelog from its settings {% icon classes="fas fa-cog" /%}.

## Placing a Changelog in the Navigation

A changelog can sit inside a [navigation group](customising-visuals/top-navigation-bar.md#navigation-structure), alongside the documentation sections and API references it belongs with, rather than on its own in the top navigation bar.

Open Manage Changelogs, select the changelog, and pick a group next to **Navigation group**. Choose **None** to take it out again. A changelog can be in one group at a time.

## Adding a Post

To add a new post to the changelog, click on New Post. Each post has a label, a slug to be accessed from, and contents. The contents of a post are the same as documentation pages and can include any block.

## Creating Posts Programmatically

You can also create and list changelog posts through the [API](/v1.0/api/ref). This is useful for publishing release notes automatically from your CI/CD pipeline.

## Editing in a Synced Repository

If your project uses [GitHub Sync](github-sync.md), your changelogs are mirrored to the repository under `changelogs/`, one folder per changelog and one file per post. You can write a release note there and review it through a pull request, and posts you write in the editor are committed back. See [Changelogs](github-sync.md#changelogs) for the file layout and frontmatter.

## RSS Feed

Changelogs can be subscribed to through an RSS feed. This enables users to remain up-to-date with all the new posts.

## Importing Posts

Posts can be imported in [markdoc format](github-sync/markdoc-format.md#changelog) by clicking the import button {% icon classes="fas fa-download" /%} next to the changelog title.

Importing posts only adds posts to the changelog. It does not remove any posts.

## Exporting Changelog

All posts in a changelog can be exported by clicking the export button {% icon classes="fas fa-upload" /%} next to the changelog title. Posts are exported in [markdoc format](github-sync/markdoc-format.md).
