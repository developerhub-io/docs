---
type: page
title: Code Theme
listed: true
slug: code-theme
description: 
index_title: Code Theme
hidden: 
keywords: 
tags: customisation
---

Natively, %product% supports a light and dark theme for code blocks. We suggest using the light code theme when using [light theme](/support-center/theme) project wide.

## Setting Light/Dark Code Theme

To change the code theme between light and dark:

- Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Under Customisation, choose the Code Theme.
- Click Save.

## Advanced Code Theming

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

We use CodeMirror for rendering and formatting our [code blocks](/support-center/code-blocks), and CodeMirror provides heaps of themes for you to choose from. The list of themes is available [here](https://codemirror.net/demo/theme.html#default).

To change the code theme, you will need to import the theme stylesheet and also provide a [setting](/support-center/advanced-settings) that specifies which theme to use. This ensures that your selected theme is applied correctly within the application.

- First, find a CDN providing the stylesheet of the theme for maximum performance. [cdnjs](https://cdnjs.com/libraries/codemirror) is an example.
- Import the theme stylesheet by add such a style tag using [auto$](/support-center/custom-javascript):

{% code %}
{% tab language="css" %}
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.60.0/theme/ambiance.min.css">
{% /tab %}
{% /code %}

- Apply the theme settings also by adding a script to your HEAD tags:

{% code %}
{% tab language="html" %}
<script>
    window.settings.apply({
      code: {
        darkTheme: 'ambiance',
        lightTheme: 'xq-light'
      }
    });  
</script>
{% /tab %}
{% /code %}

{% callout type="info" title="Note" %}
Changes will only show in live mode
{% /callout %}

{% callout type="success" title="Own themes" %}
You can also create your own themes and use them in the same way
{% /callout %}

You might want to change the styling of the code block tabs and copy button to match the theme you have chosen.