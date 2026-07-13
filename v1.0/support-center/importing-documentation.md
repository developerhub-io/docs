---
type: page
title: Importing Documentation
listed: true
slug: importing-documentation
description: 
index_title: Importing Documentation
hidden: 
keywords: 
tags: 
---

%product% provides powerful tools to enable you to easily move your content around, edit it and restructure it, all out of the editor.

## Import Sources

You can import to %product% from many sources:

- [Markdoc](/support-center/markdoc-format) export (available for entire project imports and one page imports)
- [Markdown](/support-center/external-sources#markdown-import)
- [ReadMe](/support-center/external-sources#readme-import)
- [Zendesk](/support-center/import-from-zendesk)
- Other sources, such as: [HTML](/support-center/external-sources#importing-from-html), [Confluence](/support-center/external-sources#importing-from-confluence), [Word](/support-center/external-sources#importing-from-word-documents) or [other external sources](/support-center/external-sources).

## Import a Markdoc Export

To import documentation, follow these steps:

- Make sure your import files are [structured](/support-center/importing-documentation#structuring-files) as required.
- Open Project Settings → **Import \& Export**.
- Click **Open import**.
- Choose **Markdoc**.

Importing could take a few seconds up to a minute.

{% callout type="warning" title="Legacy Darkdown exports" %}
Older DeveloperHub exports in the legacy Darkdown format are no longer accepted. Re-export your project as Markdoc and import that instead.
{% /callout %}

{% callout title="Info" %}
All imports add versions. Versions, documentations and pages are never overwritten.
{% /callout %}

## Import a page into %product%

You can import a single Markdown or a [Markdoc](/support-center/markdoc-format) page at a time into %product%.

To import one page, follow these steps:

- From the index, choose the page to import over, or create a new page and save it.
- Under the title, click on Import icon {% icon classes="fas fa-cloud-download-alt" /%}
- Choose the file to be imported.

## Structuring Files

To import documentation from %product% export into %product%, you must structure your files as such:

{% image url="https://uploads.developerhub.io/prod/02/c4ghrsdoo780zk1ii0fv0cde45vg2e8fo79ea2qu0chyak8xmu3fiie6c9ls0y5v.png" width=378 /%}

Where, for example:

- `v1.0` is the name of your version.
- `Support Center` is the title of your documentation.
- `1 Getting Started.md` is a documentation page written in Markdoc format. Its order is 1st in Support Center documentation and its title is `Getting Started`. `Getting Started` folder indicates that `1 Getting Started.md` is a parent page, and it has a subpage titled `First Steps`.
- `1 Formatting Text.md`, `2 Keyboard Shortcuts.md` and `3 Using Markdown.md` are all subpages of Writing Documentation page.
- `settings.json` is `Support Center` documentation settings file. Settings file is an optional file.

Every parent page should have a a Markdown file and a folder with the same exact name.

The orders must be incremental and starting from 1. If an order is not supplied in the file name, then no index order is guaranteed.

Additionally, you may add OpenAPI spec files in a folder named `refs` in the version folder.

All the files in the import must be compressed into a ZIP file.

## File Format

Each file contains a YAML header (frontmatter) and, for pages, optional content.

### Header

Each file contains a header depending on the index element being described.

- Page:

{% code %}
```yaml
---
type: page
title: Callouts
listed: true
slug: callouts
description: <SEO description>
index_title: Callouts
hidden: 
keywords: keyword1,keyword2
tags: tag1,tag2
---
```
{% /code %}

- Category:

{% code %}
```yaml
---
type: category
title: Start Here
---
```
{% /code %}

- Link:

{% code %}
```yaml
---
type: link
title: Go to DeveloperHub.io
url: https://developerhub.io
---
```
{% /code %}

- Separator:

{% code %}
```none
---
type: separator
---
```
{% /code %}

### Content

Category, link and separator elements do not have content. Pages do have content, written in [Markdoc](/support-center/markdoc-format): plain Markdown mixed with %product%'s block tags.

Draft and published page contents can be defined in an export and it is annotated by a `---draft` or `---published` header, such as:

{% code %}
```yaml
---draft

Draft content is here

---published

Published content is here
```
{% /code %}

### Blocks

Blocks and inline blocks are written in Markdoc tag syntax. See [Markdoc Format](/support-center/markdoc-format) for the full syntax of every block, with an example for each.

Feel free to export any page to understand the formatting of its contents.

## Image Import

If an image is referenced in Markdown format in one of the pages, it will automatically be downloaded to our servers and served from our content delivery network.

Images can be uploaded from two sources:

- HTTP, or
- Local

Regardless of the image source, each image must be at maximum 10MB in size. Otherwise, the import will fail.

{% callout type="warning" title="Warning" %}
By importing images on %product%, you are responsible to ensure that you have rights to all data.
{% /callout %}

### HTTP Image Import

To import images from the internet, they should be referenced as such:

{% code %}
```markdown
HTTP Image:

![Image Caption](https://example.com/image.png)
```
{% /code %}

It will then be downloaded from its source, and uploaded to our content delivery network. The image must be accessible online publicly, otherwise the import will fail.

### Local Image Import

To import images locally from the provided ZIP file, they must exist in a folder named `assets` alongside the versions.

They should be referenced as such:

{% code %}
```markdown
Local Image:

![Image Caption](/assets/image.png)
```
{% /code %}

Inside `assets` folder, any folder structure is allowed.
