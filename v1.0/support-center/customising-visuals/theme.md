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

It is possible to set the default theme for readers and to show a toggle for your readers to enable them to change the theme to their liking.

## Setting the theme

To change the default theme for readers:

- Open Project Settings → **Customisation**.
- Choose the theme.
- Click **Save changes** in the top menu.

{% callout type="success" title="Code Theme" %}
We suggest using the [light code theme](code-theme.md) when using the light theme.
{% /callout %}

## Show Theme Toggle

To show a theme toggle for readers:

- Open Project Settings → **Customisation**.
- Check Show Theme Toggle.
- Click **Save changes** in the top menu.

## Light Theme

{% image url="https://uploads.developerhub.io/prod/02/m8oqebybjcmrcqal8uzgoon6cu61tqsl79qa57myz7vfmb85ysga5rk52ncwvoq8.png" /%}

## Dark Theme

{% image url="https://uploads.developerhub.io/prod/02/jyanu5mrscxmmgesvv0f5dw6oliurqr50j089lw0nvxc5iv433atbtonrlwe6ez8.png" /%}

## Modifying the theme

To modify the theme, update [CSS Variables](custom-css.md#css-variables) as needed, or add your own [Custom CSS](custom-css.md). A global `.dark-mode` CSS selector is added on `document.body` when dark theme is applied.
