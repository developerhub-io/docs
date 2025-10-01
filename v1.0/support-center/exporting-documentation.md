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

- [Darkdown](/support-center/exporting-documentation#darkdown): Use if you wish to re-import the data into %product% later with no data loss.
- Markdown: Use for external purposes.

## Darkdown

[Darkdown](/support-center/importing-documentation#darkdown-format) is our flavour of Markdown. When a project is exported, and imported back, Darkdown allows the following to be retained:

- All the published and draft text in each page.
- All the blocks in each page with every configuration and detail.
- The order of the pages.
- Categories and external links.
- Documentation settings.

## Exporting a Project

To export a project:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the sidebar.
- Click Export {% icon classes="fas fa-upload" /%}. 
- Choose the export format. The active project will be exported.

It will take a few seconds, and a download will start. The downloaded file is a compressed file (zip) containing all versions, documentations, API references, and indices of the documentation. The structure of the file is as such:

{% image url="https://image-archive.developerhub.io/image/upload/7457/v3ewfbrk8hhni7blkttz/1557871252.png" mode="set" height="452.421875" width="464" %}
{% /image %}

To learn how to import this export back into %product%, check [auto$](/support-center/importing-documentation).

## Exporting a Page

To export a page:

- In the documentation index, select the page to be exported.
- Click on Export {% icon classes="fas fa-upload" /%} under the title.

The export will be in %product% [Darkdown format](/support-center/importing-documentation#darkdown-format).

## Exporting Images

To export the images you have in your %product% project, follow these steps:

- Get a [markdown export](/support-center/exporting-documentation#exporting-a-project) of your project first.
- Unzip the export.
- Use our tool [mdimg](https://github.com/developerhub-io/mdimg) which finds all the URLs in the export and downloads the images. You can find already built binaries for linux and mac in the [releases](https://github.com/developerhub-io/mdimg/releases/tag/v1.0.0).