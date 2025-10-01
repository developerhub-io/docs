---
type: page
title: External Sources
listed: true
slug: external-sources
description: 
index_title: External Sources
hidden: 
keywords: 
tags: 
---

%product% allows documentation to be imported from external sources. The documentation must be supplied in markdown format.

## How to Import Documentation?

To import documentation, follow these steps:

- Make sure your import files are structured as required.
- From the sidebar, open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}
- Click on Import {% icon classes="fas fa-download" /%}
- Choose the appropriate import source.

Importing could take a few seconds up to a minute.

You could also import a single page, see [Import a page into DeveloperHub](/support-center/importing-documentation#import-a-page-into-product) for instructions.

{% callout type="info" title="Info" %}
All imports add versions. Versions, documentations and pages are never overwritten.
{% /callout %}

{% callout type="warning" title="Limits" %}
The maximum upload size is 5MB. Contact us if your documentation has a larger size.
{% /callout %}

## Structuring Files

To import documentation from any external sources into %product%, you must structure your files as such:

{% image url="https://image-archive.developerhub.io/image/upload/-1/k6i9iufqnrhsxjnfnao2/1537921431.png" mode="responsive" height="636" width="694" %}
{% /image %}

Where:

- `v1.0` is the name of your version.
- `Support Center` is the title of your documentation.
- `Getting Started.md` is the title of a documentation page written in Markdown format. `Getting Started` folder indicates that `Getting Started.md` is a parent page, and it has a subpage titled `First Steps.md`.
- `Formatting Text.md`, `Keyboard Shortcuts.md` and `Using Markdown.md` are all subpages of Writing Documentation page.

Every parent page should have a a Markdown file and a folder with the same exact name.

Additionally, you may add OpenAPI spec files in a folder named `refs` in the version folder.

## Limitations of External Sources Import

External sources is unfortunately limited due to the lack of information in the imports. Such limitations are:

- Ordering of the pages.
- Other index elements, such as categories and external links.

## Markdown Import

To import from Markdown, you must use the file structure as shown above. The first line of any page could be a Heading 1, such as `# Title`, and will be made the page title.

### What is supported?

1. Code blocks
2. Tables
3. Images
4. Callouts (without title - Title defaults to Info)

## ReadMe Import

To import from ReadMe, you must use the file structure as shown above. All internal links will be modified to match the links in your %product% documentation.

### What is supported?

1. Multi-language code blocks
2. Tables
3. Images
4. Videos
5. Callouts
6. Embed
7. Custom HTML

### ReadMe Import Process

To import from ReadMe:

- Get an export file from ReadMe.
- Unzip the file.
- If you have any recipes or changelogs folders (or any folder that is not user-guides related) then delete them.
- Compress the version folders, and use our import tool, choosing ReadMe as import type.
- Your imported versions will be at the bottom of the version list.
- ReadMe does not provide order information in their exports, so you need to reorder the pages back manually.
- Once you are ready to publish, publish the versions!

## Importing from HTML

To import HTML, you need to convert it first to Markdown. There are many free services online that can help you convert HTML to Markdown such as [h2m](http://tinyambition.com/h2m/) or [turndown](https://domchristie.github.io/turndown/). There are also heaps of libraries available if you wish to convert many files at once. Once your docs are in markdown format, follow the [how to import documentation](/support-center/external-sources#how-to-import-documentation) guide.

## Importing from Word Documents

To import Word doc/docx format, you need to convert it first to Markdown. You can use this free online [Word to Markdown Converter](https://word2md.com/) to do that. Once your docs are in markdown format, follow the [how to import documentation](/support-center/external-sources#how-to-import-documentation) guide.

## Importing from Confluence

To import from Confluence, you need to convert it first to Markdown. Depending on how you host Confluence, there are multiple ways to export the content into Markdown including Confluence Plugins and open-source libraries.

## Importing from Zendesk

See [auto$](/support-center/import-from-zendesk).