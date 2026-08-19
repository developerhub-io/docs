---
type: page
title: Page Linking
listed: true
description: 
index_title: Page Linking
hidden: false
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

## When a Page Moves or is Renamed

Change a page's slug, rename a documentation, or [move a page](../structuring-documentation/managing-pages.md#moving-page-to-another-documentation) to another documentation, and every link to it is updated for you. Move a parent page and links to its subpages follow too.

{% callout type="warning" title="The old URL does not redirect" %}
This fixes the links inside your documentation. It does not leave a redirect behind, so anyone reaching the old URL from a bookmark, an external site, or a search result will land on your [404 page](../landing-page.md#404-page). Worth weighing before you change the slug of a page that already ranks.
{% /callout %}

{% callout title="Link pages, do not paste URLs" %}
Only links made with page linking are updated. A full URL you paste in as an external link is left exactly as you wrote it, so it will break when that page moves.
{% /callout %}

## How to Link Pages?

To create a link between pages, type `@` to open the pages selector.

{% image url="../../../assets/9fab2f8b4eb2913fdae1797d72cc26013c6aaa37.png" /%}

A list of all pages under the version will be listed for you to choose from. Search through the list by typing down the page name or slug. To select a page, click on its name in the list. If you are selecting an API Reference, then you'll find the title of the API Reference.

Alternatively, you can also link to an internal page by highlighting text and clicking on the link icon.

{% callout title="External vs Page link" %}
External links in the editor show with a top-right pointing arrow so you can tell them apart from page links. The arrow will not show in live mode.
{% /callout %}

## Changing Link Title/Specifying Heading

After selecting the page, you will be prompted to optionally link to a specific heading if you selected a page, or link to a specific operation if you selected an API reference.

{% image url="../../../assets/eed5b973e247512d44a9f3af31ce616a2f1dd6a4.png" /%}

If you want to jump to a certain heading in a page, you can specify it. Start typing to find a heading in the page you selected, or click on the arrow to view all. Leaving **Heading** empty will default to jumping to the title of the page. The same goes for API references, where you can select a specific operation to jump to.

Once you select a heading/operation, its URL fragment will appear. A fragment is the part of the link that is after the hash sign `#` . For example, the link `https://pied-piper.developerhub.io/v1.0/middle-compression/intro#how-to-use` has the fragment `how-to-use`.

Fragment can only contain alphanumeric characters and hyphens.

{% callout title="Info" %}
We do not monitor changes to the headings/operations. If a heading/operation is changed, then you should create the link again.
{% /callout %}

{% callout title="Following a link" %}
To open a link's target while editing, click the link to bring up its toolbar, then use the open control or hit {% key key="⇧" /%} while clicking on it. A modifier-click (such as {% key key="⌘" /%} / {% key key="Ctrl" /%} or {% key key="⇧" /%}) opens it in a new tab.
{% /callout %}

## Analyse Links

Analysing links helps you understand the links that are:

- Broken because the linked page/reference was deleted.
- Leading to an unpublished page/reference from a published page.
- Have an internal %product% link, instead of a link to your published docs.

## Listing Broken Links

If a page contains links with issues, a badge will appear next to the page actions in the navigation bar. Link analysis runs automatically every time a page loads.

Links with issues are also underlined in the editor:

- Orange underline indicates a warning or lower-severity issue.
- Red underline indicates a higher-severity issue (for example, a broken or unreachable link).

### Analyse Links for Entire Version

You can analyse all links in a version at once by:

- Open Manage Versions (version menu → settings {% icon classes="fas fa-cog" /%} cog).
- Select the version.
- In the Lifecycle card, click **Check broken links**.

{% image url="../../../assets/41212df03ac31b498327a43baa62d246b7aaec5f.jpeg" /%}

### View Broken Links in a Page

To view all the links analysis in a page, either click on the notification under the page title or:

- From the right sidebar, open **Page Info** {% icon classes="fas fa-info-circle" /%}.
- Open the **Links** tab and review the broken links and issues under **Link issues**.

{% image url="../../../assets/3638384f303b1419e52cd1627031883cf0831c13.png" %}
Link issues in the Links tab
{% /image %}

Every broken link will show you the title and the heading (if any) that it had before breaking. The list also shows the current text of the link so you are able to find it and fix it.

Under **Link issues**, click an issue to view the link it refers to.

{% callout title="404 Page" %}
Broken page links lead to [404 Page](../landing-page.md#404-page).
{% /callout %}

{% callout title="Only Internal Links" %}
Only internal links created by using Page Linking are examined for breaking. The monitoring tool will not examine or alert about external links leading to 404.
{% /callout %}

### Broken Links Email

A bi-weekly email is sent to admins and publishers that lists all the broken links in the docs. An email is sent per project and a maximum of 3 emails is sent per user. The email subscription status can be changed from [Account Settings](../account-settings.md).

Admins can also turn the report off for a whole project from Project Settings → **Advanced** → **Notifications**, by unchecking **Broken links report email**. See [Advanced Settings](../project-settings/advanced-settings.md#broken-links-report-email).

## Listing Linked Pages (Backlinks)

If you are planning to delete a page, or modify the page heavily, then you might want to know what other pages are depending on this page. To list all pages linking to the current page you are on:

- From the right sidebar, open **Page Info** {% icon classes="fas fa-info-circle" /%}.
- Open the **Links** tab. Linked pages load automatically.
- Any linked pages are listed under **Pages linked**.

{% image url="../../../assets/8d14fb27b3ea9e3f1571ef923aed2299c0ecc75a.png" %}
Pages linked in the Links tab
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
