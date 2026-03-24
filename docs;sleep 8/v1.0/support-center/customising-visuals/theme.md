---
type: page
title: Theme
listed: true
slug: theme
description: 
index_title: Theme
hidden: 
keywords: 
tags: customisation
---

Docs in %product% can have two themes:

- Light theme {% icon classes="far fa-sun" /%}
- Dark theme {% icon classes="fas fa-moon" /%}

It is possible to set the default theme for readers and to show a toggle for your readers to enable them to change the theme to their liking.

## Setting the theme

To change the default theme for readers:

- Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Under Customisation, choose the theme.
- Click Save.

{% callout type="success" title="Code Theme" %}
We suggest using the [light code theme](/support-center/code-theme) when using the light theme.
{% /callout %}

## Show Theme Toggle

To show a theme toggle for readers:

- Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Under Customisation, check Show Theme Toggle.
- Click Save.

## Light Theme

{% image url="https://uploads.developerhub.io/prod/02/m8oqebybjcmrcqal8uzgoon6cu61tqsl79qa57myz7vfmb85ysga5rk52ncwvoq8.png" mode="responsive" height="1846" width="3110" %}
{% /image %}

## Dark Theme

{% image url="https://uploads.developerhub.io/prod/02/jyanu5mrscxmmgesvv0f5dw6oliurqr50j089lw0nvxc5iv433atbtonrlwe6ez8.png" mode="responsive" height="1846" width="3110" %}
{% /image %}

## Modifying the theme

To modify the theme, update [CSS Variables](/support-center/custom-css#css-variables) as needed, or add your own [auto$](/support-center/custom-css). A global `.dark-mode` CSS selector is added on `document.body` when dark theme is applied.