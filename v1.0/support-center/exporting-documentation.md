---
type: page
title: Exporting Documentation
listed: true
slug: exporting-documentation
description: 
index_title: Exporting Documentation
hidden: 
keywords: 
tags: 
---

Your data is your data. You can always export it at any time.

We provide project exports in two formats:

- [Markdoc](/support-center/exporting-documentation#markdoc): Use if you wish to re-import the data into %product% later with no data loss.
- Markdown: Use for external purposes.

You can also export a version to [PDF](/support-center/pdf-export).

## Markdoc

[Markdoc](/support-center/markdoc-format) is the markdown-based format %product% uses for pages. When a project is exported, and imported back, Markdoc allows the following to be retained:

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

To learn how to import this export back into %product%, check [Importing Documentation](/support-center/importing-documentation).

## Exporting a Page

To export a page:

- In the documentation index, select the page to be exported.
- Click on Export {% icon classes="fas fa-upload" /%} under the title.
- Choose the export format: Markdoc, Markdown or Word.

If you plan to re-import the page into %product% later with no data loss, use [Markdoc format](/support-center/markdoc-format).

## Exporting Images

To export the images you have in your %product% project, follow these steps:

- Get a [markdown export](/support-center/exporting-documentation#exporting-a-project) of your project first.
- Unzip the export.
- Use our tool [mdimg](https://github.com/developerhub-io/mdimg) which finds all the URLs in the export and downloads the images. You can find already built binaries for linux and mac in the [releases](https://github.com/developerhub-io/mdimg/releases/tag/v1.0.0).
