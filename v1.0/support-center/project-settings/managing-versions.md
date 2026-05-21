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

## Manage Versions

Most version actions live on the **Manage Versions** page. To open it:

- In the editor top navigation, click on the version menu.
- Click the settings {% icon classes="fas fa-cog" /%} cog.

The left list shows every version in the project. Select a version to see and edit its settings on the right.

## Creating Versions

To create a new version:

1. Open the version menu in the top navigation.
2. Click **+ New version**.
3. Give it a name.
4. Choose **Clone from current version** to copy every documentation and page from the current version, or **Create from scratch** to start empty.

{% callout type="success" title="What has happened?" %}
When you clone a version, every documentation, API reference and page under the source version is copied to the new version.
{% /callout %}

## Publishing Versions

Versions by default are not published. To publish (or unpublish):

- Open the version menu in the top navigation, then select the version.
- In Manage Versions, toggle **Published** in the Visibility card or use the **Publish** / **Unpublish** button in the header.

When a version gets published, only published documentation and API references in the version would be viewable by readers. Unpublishing a version makes the version and all its contents unviewable by readers, but it does not modify the publish state for its documentation and API references.

Unpublished versions show an `Unpublished` pill on the version menu and in the Manage Versions list.

## Deleting Versions

To delete a version:

1. Open Manage Versions.
2. Select the version to delete.
3. In the Danger zone card, click **Delete version**.
4. Confirm your deletion.

{% callout type="warning" title="Warning" %}
Once a version is deleted, it cannot be retrieved back.
{% /callout %}

## Ordering Versions

To change a version order in the picker:

- Open Manage Versions.
- Drag the version from the handle {% icon classes="fas fa-grip-vertical" /%}.
- Drop the version in the desired place.

If the version is ordered first and is published, then it will be the default version to load for your readers.

The default version does not show its slug in the live page links, for example, if version 1.0 was default for this documentation project then:

`https://docs.developerhub.io/support-center/managing-versions` would implicitly mean that it should load the default version, which is version 1.0. Using `https://docs.developerhub.io/v1.0/support-center/managing-versions` would yield the same result.

## Moving Readers to New Version

If your readers have bookmarked pages from older versions, or are unaware that your documentation is versioned, then you might want to notify them using a banner at the top of the page that there is a newer version. You can do so using [an advanced setting](/support-center/advanced-settings) by setting `warnings.oldVersion` to `true`.

{% image url="https://image-archive.developerhub.io/image/upload/v2_1/mo0dxqrzmkjs8qkq8rra/1621206651.png" caption="Banner suggesting to the reader that there's a newer version" mode="responsive" height="656" width="1249" %}
{% /image %}

## Locking Versions

Versions can be locked when they no longer should have their documentation and API references editable. When a version is locked, documentation and API references cannot be:

- Created.
- Edited.
- Removed.
- Published.

This also applies to changes made using the [auto$](/v1.0/api/ref).

To lock or unlock a version:

- Open Manage Versions.
- Select the version.
- In the Visibility card, toggle **Locked**.

A `Locked` pill shows on the version menu and in the Manage Versions list. The Save draft and Publish buttons in pages are replaced by a disabled "Locked" button.

## Version Reports

Version reports can be downloaded which includes a list of all pages with the following information:

- Title
- Creator
- Updater
- Created date
- Updated date
- Is in draft state
- Is published

To download a version report:

- Open Manage Versions.
- Select the version.
- In the Lifecycle card, click **Download** next to Pages report.