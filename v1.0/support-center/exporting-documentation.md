---
type: page
title: Exporting Documentation
listed: true
description: 
index_title: Exporting Documentation
hidden: false
keywords: 
tags: 
---

Your data is your data. You can always export it at any time.

We provide project exports in two formats:

- [Markdoc](exporting-documentation.md#markdoc): Use if you wish to re-import the data into %product% later with no data loss.
- Markdown: Use for external purposes.

You can export the whole project, a single [version](exporting-documentation.md#exporting-a-version), or an individual [page](exporting-documentation.md#exporting-a-page). A whole version can be exported to [PDF](pdf-export.md), and a single page to [its own PDF](exporting-documentation.md#exporting-a-page-to-pdf).

## Markdoc

[Markdoc](github-sync/markdoc-format.md) is the markdown-based format %product% uses for pages. When a project is exported, and imported back, Markdoc allows the following to be retained:

- All the published and draft text in each page.
- All the blocks in each page with every configuration and detail.
- The order of the pages.
- Categories and external links.
- Documentation settings.

## Exporting a Project

To export a project:

- Open Project Settings → **Import \& Export**.
- Click the export format you want. The active project will be exported.

It will take a few seconds, and a download will start. The downloaded file is a compressed file (zip) containing all versions, documentations, API references, and indices of the documentation. The structure of the file is as such:

{% image url="https://uploads.developerhub.io/prod/02/anun2ah7qx47rehzb8jcfq5717vkc314t328e9de6lnjmo3ouk1cygrcln2brpvt.png" width=464 /%}

To learn how to import this export back into %product%, check [Importing Documentation](importing-documentation.md).

## Exporting a Version

You can also export a single version on its own:

- Open **Manage Versions** (version menu → settings {% icon classes="fas fa-cog" /%} cog).
- Select the version.
- Under **Lifecycle**, choose **Export as Markdoc** for a full-fidelity zip you can re-import with no data loss, or **Export as Markdown** for a portable zip for external use.

The download is a zip named after the version, containing that version's documentations, pages, and API references. Project-wide changelogs are not included in a single-version export; use a [project export](exporting-documentation.md#exporting-a-project) if you need them.

The same card also offers **Export as PDF** (see [PDF Export](pdf-export.md)).

## Exporting a Page

To export a page:

- In the documentation index, select the page to be exported.
- Click on Export {% icon classes="fas fa-upload" /%} under the title.
- Choose the export format: Markdoc, Markdown, Word or PDF.

If you plan to re-import the page into %product% later with no data loss, use [Markdoc format](github-sync/markdoc-format.md).

### Exporting a Page to PDF

A single-page PDF downloads as soon as it is ready, named after the page. It contains the page on its own: the title, the body, and a page number on each sheet so a printed hand-out collates. The navigation index, the table of contents, and the covers and banners of a [version PDF](pdf-export.md) are all left out. Tabs and accordions are laid out open, so nothing stays hidden inside a collapsed section.

You get the draft you are looking at, the same as the other formats in the menu. [Conditional content](conditional-content.md) is resolved as an anonymous reader would see it, so blocks restricted to an audience are left out.

Single-page PDF export needs the same plan as [PDF Export](pdf-export.md). Where it is not available, PDF does not appear in the export menu.

## Printing a Page

Any page can be printed straight from the browser with Ctrl+P (Cmd+P on a Mac), on your published documentation as well as in the editor. The printed copy keeps the page content and drops the interface around it: the navigation index, the table of contents, the top bar, and the copy button on code blocks. Pages always print on a light background, even when you or your reader is viewing in dark mode.

{% callout type="warning" title="Code blocks when printing" %}
Code blocks stay dark in both themes, and browsers leave background fills out of printed output by default. Tick **Background graphics** in your browser's print dialog to have them come out readable.
{% /callout %}

## Exporting Images

To export the images you have in your %product% project, follow these steps:

- Get a [markdown export](exporting-documentation.md#exporting-a-project) of your project first.
- Unzip the export.
- Use our tool [mdimg](https://github.com/developerhub-io/mdimg) which finds all the URLs in the export and downloads the images. You can find already built binaries for linux and mac in the [releases](https://github.com/developerhub-io/mdimg/releases/tag/v1.0.0).
