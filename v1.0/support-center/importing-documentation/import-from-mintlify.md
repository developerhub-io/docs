---
type: page
title: Import from Mintlify
listed: true
description: 
index_title: Import from Mintlify
hidden: false
keywords: 
tags: 
---

Moving from Mintlify? %product% reads your documentation straight from GitHub and brings it across: your pages, your images, your API references, and the look of your site.

## Before You Start

- You need the **Publisher** [role](../collaboration.md) or above.
- Your documentation must be in a GitHub repository. Private ones are fine.

## Importing from Mintlify

1. Open Project Settings → **Import \& Export**.
2. Under **Bring content in**, click **Mintlify**.
3. Paste the address of your repository, such as `github.com/acme/docs`.
4. Click **Start import**.

Paste any page of the repository and we work out the rest. If your documentation sits on another branch, or in a folder of its own, open **Advanced** and say where.

## Before Anything is Created

%product% reads your site first and reports what it found: how many pages, and the sections, versions and languages they sit in. Nothing is created at this stage.

You also get **What will change on the way in**, a list of anything that cannot come across exactly as it is. It is worth reading before you start.

## Choosing Versions and Languages

If your site has more than one version or language, you choose which of them come over. Each one becomes a version of its own in %product%.

Tick the ones you want and leave the rest. Run the import again later to bring in the others.

## What Comes Across

Your pages arrive as pages, with your sections and groups around them. Callouts, tabs, accordions, cards, steps and code samples all have an equivalent here, and anything without one keeps its text.

Images are re-hosted on our content delivery network, so they keep working once Mintlify is switched off. Links between your pages are rewritten to their new addresses, and your OpenAPI files become [API references](../api-references.md).

## What Changes in Your Project

An import brings your Mintlify site's appearance with it: title, colours, logo, favicon, font, top bar links, footer and redirects. **These replace what your project has now.** Import into a new project if you would rather keep the way yours looks.

## After the Import

Worth checking before you publish:

- **Warnings.** Everything that changed on the way in is listed when the run finishes.
- **Where your pages landed.** An import adds new versions rather than filling in the one you have open.
- **Structure.** Mintlify divides content differently to %product%, so you may want to [restructure the pages](../structuring-documentation/managing-pages.md).

## Stopping an Import

Click **Stop import** while a run is in progress. Everything imported up to that point stays in your project.

{% callout title="Info" %}
Imports always add versions. Existing versions, sections and pages are never overwritten. Running an import twice gives you two copies rather than updating the first.
{% /callout %}
