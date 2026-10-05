---
type: page
title: Theme
listed: true
description: 
index_title: Theme
hidden: false
keywords: 
tags: customisation
---

Docs in %product% can have two themes:

- Light theme {% icon classes="far fa-sun" /%}
- Dark theme {% icon classes="fas fa-moon" /%}

It is possible to set the default theme for readers, or let it follow each reader's system setting, and to show a toggle for your readers to enable them to change the theme to their liking.

## Setting the theme

To change the default theme for readers:

- Open Project Settings → **Customisation**.
- Next to **Theme**, choose **Light**, **Dark** or **Auto**. Auto shows each reader the theme their system is set to.
- Click **Save changes** in the top menu.

New projects start on **Auto**.

{% callout type="success" title="Code Theme" %}
We suggest using the [light code theme](code-theme.md) when using the light theme.
{% /callout %}

## Show Theme Toggle

To show a theme toggle for readers:

- Open Project Settings → **Customisation**.
- Check Show Theme Toggle.
- Click **Save changes** in the top menu.

## Light Theme

{% image url="../../../assets/reader-theme-light.png" /%}

## Dark Theme

{% image url="../../../assets/reader-theme-dark.png" /%}

## Modifying the theme

To modify the theme, update [CSS Variables](custom-css.md#css-variables) as needed, or add your own [Custom CSS](custom-css.md). A global `.dark-mode` CSS selector is added on `document.body` when dark theme is applied.
