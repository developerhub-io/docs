---
type: page
title: Managing Versions
listed: true
slug: managing-versions
description: 
index_title: Managing Versions
hidden: 
keywords: 
tags: 
---

Using %product%, you can version your documentations. The default version is called v1.0, it is up to you to define how you call your versions. Semantic versioning is not required, so you can use words such as "beta", "alpha" and "latest" along actual version numbers.

Versioning is very powerful. When pages are [linked](/support-center/page-linking) inside a version, and that version is cloned, all the page links are updated accordingly to the match the new version.

## Creating Versions (Cloning)

New versions are always cloned from other versions, to clone a version:

1. Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
2. Select the version to clone from.
3. Click on "Clone from current version".

{% callout type="success" title="What has happened?" %}
Nice, you cloned a version. That means that every documentation and page under that version has been copied  to the new version.
{% /callout %}

## Publishing Versions

Versions by default are not published. Once you are ready to publish (or to unpublish):

1. Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
2. Below the version title at the top, click on the publishing state and modify it as needed.

When a version gets published, only published documentation and API references in the version would be viewable by readers. Unpublishing a version makes the version and all its contents unviewable by readers, but it does not modify the publish state for its documentation and API reference.

When a version is published, it will appear with a green dot {% icon classes="fas fa-circle green-text" /%} next to it in the sidebar. When the version is unpublished, it will appear with a red dot {% icon classes="fas fa-circle red-text" /%} next to it.

## Deleting Versions

To delete a version:

- Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
- Select the version to delete.
- Click on the red bin {% icon classes="far fa-trash-alt red-bg-icon" /%} next to the Version title at the top.
- Confirm your deletion.

{% callout type="warning" title="Warning" %}
Once a version is deleted, it cannot be retrieved back.
{% /callout %}

## Ordering Versions

To change a version order in the picker:

- Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
- Drag the version to be ordered from the handle {% icon classes="fas fa-grip-vertical" /%}
- Drop the version in the desired place.

If the version is ordered first and is published, then it will be the default version to load for your readers. A default badge would show to indicate that it is default.

The default version does not show its slug in the live page links, for example, if version 1.0 was default for this documentation project then:

`https://docs.developerhub.io/support-center/managing-versions` would implicitly mean that it should load the default version, which is version 1.0. Using `https://docs.developerhub.io/v1.0/support-center/managing-versions` would yield the same result.

## Moving Readers to New Version

If your readers have bookmarked pages from older versions, or are unaware that your documentation is versioned, then you might want to notify them using a banner at the top of the page that there is a newer version. You can do so using [an advanced setting](/support-center/advanced-settings) by setting `warnings.oldVersion` to `true`.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1621206651/v2_1/mo0dxqrzmkjs8qkq8rra.png" caption="Banner suggesting to the reader that there's a newer version" mode="responsive" height="656" width="1249" %}
{% /image %}

## Locking Versions

Versions can be locked when they no longer should have their documentation and API references editable. When a version is locked, documentation and API references cannot be:

- Created.
- Edited.
- Removed.
- Published.

This also applies to changes made using the [auto$](/v2.0/api/ref).

To lock/unlock a version:

- Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
- Select the version to be locked/unlocked.
- Open the version settings {% icon classes="fas fa-cog" /%}.
- Check or uncheck the setting Locked.

A lock icon would show next to the locked version and the buttons to save drafts or publish would be replaced by a button having "Locked" on it.