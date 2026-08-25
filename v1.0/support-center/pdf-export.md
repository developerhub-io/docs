---
type: page
title: PDF Export
listed: true
description: 
index_title: PDF Export
hidden: false
keywords: 
tags: 
---

{% html %}
<div class="grow-border text-left">
<div class="grow-star">🪐</div>
    Available in Enterprise. Also purchasable as an add-on to non-enterprise plans.
</div>
{% /html %}

If your readers cannot access the documentation online, then you can provide them with a PDF export of the documentation.

This page covers exporting a version, or the sections of it you choose. To export a single page as a PDF, see [Exporting a Page to PDF](exporting-documentation.md#exporting-a-page-to-pdf).

{% image url="https://uploads.developerhub.io/prod/02/yhzfvuhxf6u64mvnb50m5va3jxlbraqdtoqf7vmk828xr77mqb0byw2g1ads6rck.png" /%}

## How to export to PDF?

PDF export has a settings pane of its own: Project Settings → **Import \& Export** → **PDF**. Everything to do with PDFs lives there, namely what a PDF covers, the builds you have already generated, and how they all look.

To generate a PDF:

1. Open Project Settings → **Import \& Export**, then under **Take content out** click **PDF**.
2. In the **In this PDF** card, pick the **Version** you are exporting.
3. Tick the documentation sections and API references you want included.
4. Click **Generate PDF**.

{% image url="../../assets/pdf-export-pane.png" /%}

The build appears in the **Generated PDFs** card below and moves through Queued and Building. Once it reads Ready, click **Download**.

Two shortcuts open the pane with the selection already made for you:

- Manage Versions (version menu → settings {% icon classes="fas fa-cog" /%} cog) → select the version → **Export as PDF**, which preselects that version.
- Manage Sections (section menu → settings {% icon classes="fas fa-cog" /%} cog) → select the documentation section or API reference → **Export as PDF**, which preselects that one section on its own.

## Choosing What the PDF Covers

The **In this PDF** card is the outline of the document. Its rows run in the order they appear in the PDF: the cover page, the table of contents, your documentation sections, your API references, and the back pages. Untick anything you want left out and it visibly drops out of the outline.

- Every published documentation section and API reference starts ticked, so generating without changing anything gives you the whole version, exactly as it always did.
- Use **Select all** or **Clear all** on the **Documentation** and **API references** headings to tick or clear a whole group at once.
- Unpublished sections are listed too, marked with an **Unpublished** pill, and start unticked. You can still include them deliberately.
- The cover page, table of contents and back pages are always part of the document, so they cannot be unticked. They come from PDF appearance.

At least one section has to be ticked; **Generate PDF** stays disabled until one is.

{% callout type="warning" title="Including unpublished sections" %}
Unpublished sections export their last published content. Pages that have never been published come out with their title and no body.
{% /callout %}

Every build remembers what it covered, and the **Generated PDFs** list names those sections against it, or reads **All sections** for a whole-version export. So you can keep a full manual and a shorter extract side by side and still tell them apart.

## PDF Permalink

After you have at least one PDF generated, you can generate a permalink for PDF downloads of the version. The permalink would always download the latest PDF that you have generated. You can use that link publicly if you wish to allow your readers to download the latest PDF.

To get a permalink, open Project Settings → **Import \& Export** → **PDF**, select the version, and click **Copy permalink** in the **Generated PDFs** card. The URL will be copied to your clipboard.

{% callout type="warning" title="Unique link" %}
The permalink is a unique link that cannot be revoked once someone has the link. Make sure you share the permalink with the right audience.
{% /callout %}

## Contents of the PDF

Our exported PDFs contain the following in order:

- A cover page, if you provide one,
- A page containing the project title and version name,
- Table of contents,
- The documentation sections you included,
- The API references you included,
- Back pages, if you provide them.

## Customisation of PDF

The **PDF appearance** card holds the parts that apply to every PDF the project generates, so it sits apart from the section picker. It is collapsed by default and shows a summary of what is currently set; click **Edit** to open it.

You can set these yourself:

- **Cover page**: a link to a PDF placed before the contents.
- **Back pages**: links to PDFs appended after the content, one URL per line.

Both take a URL that ends in `.pdf`. Click **Save** once you are done. A change here takes effect on the next PDF you generate, so it does not alter the builds you already have.

The logo at the top of each page and the footer banner are shown in the same card but are not editable there. To add or change either, [contact us](contact-us.md) with the assets.

## Limitations of PDF

- The PDFs are not interactive: The links in pages do not reference other pages in the PDF.
- Your project must be accessible through the custom domain, or the subdomain if the custom domain is not set.

## Troubleshooting Failed Exports

There are specific circumstances when a PDF export might fail. Rest assured that if a PDF export fails, we get notified of it and we can provide you with more information about its failure.

If your docs are hosted behind a firewall, make sure to whitelist `DeveloperHub.io PDF Exporter` user agent.

## Example of PDF

Download our own latest PDF of our docs:

{% html %}
<a href="https://api.developerhub.io/api/public/version/1/pdf-download?k=097d1d25d69fa22042742340148c45004d162144ed0955ba8196c8f0dfc69d8e" 
   target="_blank" 
   style="background-color: var(--brand); color: white; padding: 12px; border-radius: 3px; text-decoration: none !important">
    Download PDF
</a>
{% /html %}
