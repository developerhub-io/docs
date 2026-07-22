---
type: page
title: Publishing Documentation
listed: false
description: 
index_title: Publishing Documentation
hidden: false
keywords: 
tags: 
---

Documentations are contained within versions and are published in versions.

To have your documentation available online for the public to read:

1. Open Manage Versions (version menu → settings {% icon classes="fas fa-cog" /%} cog).
2. Select the right version.
3. Click **Publish**.

{% callout type="success" title="Wow!" %}
All the documentations under that version are now available for everyone to read them!
{% /callout %}

## Broken Link Check before Publishing

When you publish a version that is not yet public, %product% scans it for broken links first, so readers don't hit them the moment the version goes live. The **Publish** button shows **Checking links…** while it scans.

- If nothing is broken, the version publishes straight away.
- If there are broken links, a dialog opens listing them, grouped by documentation (with a separate group for **API References**). Each row links to the page that contains the link, so you can jump to it and fix it.
- Choose **Publish anyway** to go live without fixing them, or **Cancel** to keep editing.

Only broken links stop to ask you. Softer warnings, such as links to unpublished pages, are shown alongside for context but never block publishing.

{% callout title="Check links any time" %}
You don't have to wait until you publish. In **Manage Versions**, under **Lifecycle**, use **Check links** to scan the selected version for broken links at any time.
{% /callout %}

## Unpublishing

To unpublish your documentation and stop public access:

1. Open Manage Versions (version menu → settings {% icon classes="fas fa-cog" /%} cog).
2. Select the right version.
3. Click **Unpublish**. You will be prompted to confirm.

{% callout type="warning" title="Warning" %}
A crow 🐦  telling the reader that there is nothing to see on this page will show if a reader tries to access an unpublished documentation
{% /callout %}
