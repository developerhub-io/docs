---
type: page
title: Documentation Settings
listed: true
slug: documentation-settings
description: 
index_title: Documentation Settings
hidden: 
keywords: 
tags: 
---

Each documentation can have different settings. These settings affect their function. Documentation [publishing state](/support-center/managing-documentation#publishing-documentation) can also be controlled.

{% callout type="warning" title="Deprecation (11 Dec 2023)" %}
Minimal layout is no longer supported. Only wide layout is available. Also, index is always scrollable.
{% /callout %}

## Description

You may manually set a description for your Documentation. The description will be read by search engines and shown in search results. To set the description:

- In your sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Edit the documentation description.

## Collapsible Index

By default, the index of your documentation is all expanded. That means that the child pages (second-level pages) are always showing.

If your documentation has a long index, you might want to consider setting the index to collapsible. To achieve that:

- In your sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Check "Can parent pages indices collapse?" option.

{% callout type="info" title="Only in live mode" %}
The index will always be expanded in edit mode. This setting only has an effect in live mode.
{% /callout %}

## Collapsible Categories

By default, all categories of your documentation would be expanded.

To change this behaviour and allow categories to be collapsed:

- In your sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Check "Can categories collapse?"

{% callout type="info" title="Manually Toggle Categories?" %}
If you want the categories to be manually toggle-able, add a [HEAD tag](/support-center/custom-javascript) containing a script with `window.settings.categoryToggle = true`.
{% /callout %}

## Show Page Last Updated

To enable your readers to see who updated the page last, and when was it updated, you can enable Show Page Last Updated setting. To achieve that:

- In your sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Change "Show page last updated?" to one of **Disabled**, **Date & author** or **Date only**.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1585424716/12016/fzm4ex8ao3vkbo84hlht.jpg" mode="responsive" height="443" width="839" %}
{% /image %}

## Copy Documentation to Version

If needed, you can copy a documentation section to a version. The same documentation slug should not exist in the destination version. To copy the documentation section to a version:

- In your sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Click on Copy to Version and select the version.