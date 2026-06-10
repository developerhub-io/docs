---
type: page
title: Page Linking
listed: true
slug: page-linking
description: 
index_title: Page Linking
hidden: 
keywords: 
tags: 
---

Linking to pages (cross-referencing) is very powerful. It ensures that the pages hierarchy is always correct by automatically updated references as your documentation scales and changes. Linking to pages applies between pages in one version.

{% callout type="success" title="Page or API" %}
You can link to a page or to an API reference - everything written here applies for both.
{% /callout %}

## Why to Link Pages?

When a page is linked inside a version:

- The link will follow the page regardless of changes in documentation or page name.
- On cloning versions, the link will follow the page in the new version.
- You will be notified if a link breaks because a page was deleted.

## How to Link Pages?

To create a link between pages, type `@` to open the pages selector.

{% image url="https://uploads.developerhub.io/prod/02/kf6unx2cloets13zb93tf93cholub4q1cvs9gjt8lcwpt1i1323trusuun4t173y.gif" caption="Pages selector open" mode="600" height="490" width="600" %}
{% /image %}

A list of all pages under the version will be listed for you to choose from. Search through the list by typing down the page name or slug. To select a page, click on its name in the list. If you are selecting an API Reference, then you'll find the title of the API Reference.

{% callout type="info" title="External vs Page link" %}
External links in the editor show with a top-right pointing arrow so you can tell them apart from page links. The arrow will not show in live mode.
{% /callout %}

## Changing Link Title/Specifying Heading

After selecting the page, you will be prompted to change the link text (title) and optionally to link to a specific heading if you selected a page, or link to a specific operation if you selected an API reference.

**Note**: If you do not specify a title, then the title will _automatically_ update whenever the linked page title changes. For example, if you linked to page "Getting Started", and then you modified "Getting Started" page title into "Welcome", then the link text will automatically change to "Welcome".

{% image url="https://uploads.developerhub.io/prod/02/78pl37gpanmd2ml1pckb4zj0i7z5p2748zkwxlqaj99bvb9ocvsu00nrx7rwjprm.jpg" caption="Changing link title and specifying heading" mode="responsive" height="303" width="760" %}
{% /image %}

If you want to jump to a certain heading in a page, you can specify it. Start typing to find a heading in the page you selected, or click on the arrow to view all. Leaving **Heading** empty will default to jumping to the title of the page. The same goes for API references, where you can select a specific operation to jump to.

Once you select a heading/operation, its URL fragment will appear. A fragment is the part of the link that is after the hash sign `#` . For example, the link `https://pied-piper.developerhub.io/v1.0/middle-compression/intro#how-to-use` has the fragment `how-to-use`.

Fragment can only contain alphanumeric characters and hyphens.

{% callout type="info" title="Info" %}
We do not monitor changes to the headings/operations. If a heading/operation is changed, then you should create the link again.
{% /callout %}

{% callout type="info" title="Keyboard Shortcut" %}
Did you know that you can follow the link when in editor mode by holding Shift +  ⇧  and clicking on the link?
{% /callout %}

## Analyse Links

Analysing links helps you understand the links that are:

- Broken because the linked page/reference was deleted.
- Leading to an unpublished page/reference from a published page.
- Have an internal %product% link, instead of a link to your published docs.

## Listing Broken Links

If a link between pages or references is unreachable, then you will be notified below the page title of the link analysis results. Link analysis runs automatically every time a page loads.

{% image url="https://uploads.developerhub.io/prod/02/5hkvxafayenzwmuf79oo94uc2ha9lhocfkc7jspmlg3y5nmfp9kh0pr4l4l621jv.jpg" caption="Broken link notification" mode="responsive" height="1058" width="2268" %}
{% /image %}

### Analyse Links for Entire Version

You can analyse all links in a version at once by:

- Open Manage Versions (version menu → settings {% icon classes="fas fa-cog" /%} cog).
- Select the version.
- In the Lifecycle card, click **Check broken links**.

{% image url="https://uploads.developerhub.io/prod/02/l6ai84yx1otyv04k7z51eodgqap3ebyi4orv9c14ixlfwy2clv9iuiq75o1xf8ia.jpg" mode="responsive" height="321" width="720" %}
{% /image %}

### View Broken Links in a Page

To view all the links analysis in a page, either click on the notification under the page title or:

- From the right sidebar, open **Page Info** {% icon classes="fas fa-info-circle" /%}.
- Open the **Links** tab and review the broken links and issues under **Link issues**.

{% image url="asset:0qvxa6ixoxml" caption="Link issues in the Links tab" mode="responsive" height="441" width="464" %}
{% /image %}

Every broken link will show you the title and the heading (if any) that it had before breaking. The list also shows the current text of the link so you are able to find it and fix it.

{% callout type="info" title="404 Page" %}
All broken page links will have the HREF of "/-" which leads to a 404 page.
{% /callout %}

{% callout type="info" title="Only Internal Links" %}
Only internal links created by using Page Linking are examined for breaking. The monitoring tool will not examine or alert about external links leading to 404.
{% /callout %}

### Broken Links Email

A bi-weekly email is sent to admins and publishers that lists all the broken links in the docs. An email is sent per project and a maximum of 3 emails is sent per user. The email subscription status can be changed from [auto$](/support-center/account-settings).

## Listing Linked Pages (Backlinks)

If you are planning to delete a page, or modify the page heavily, then you might want to know what other pages are depending on this page. To list all pages linking to the current page you are on:

- From the right sidebar, open **Page Info** {% icon classes="fas fa-info-circle" /%}.
- Open the **Links** tab. Linked pages load automatically.
- Any linked pages are listed under **Pages linked**.

{% image url="asset:0qvxa6ixoxml" caption="Pages linked in the Links tab" mode="responsive" height="441" width="464" %}
{% /image %}

## Page Permalinks

Permalinks are links that never change providing a reliable reference to a page.

To get a page permalink:

- From the right sidebar, open **Page Info** {% icon classes="fas fa-info-circle" /%}.
- Click the permalink button {% icon classes="fas fa-link" /%} in the panel header.
- The link will be copied to your clipboard.

Our permalinks have the following structure: `https://<domain>/_permalink/<id>`.

{% callout type="warning" title="Warning" %}
Permalinks are dependant on the custom domain used. If the custom domain changes, the permalink will not be valid anymore.
{% /callout %}