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

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

We use CodeMirror for rendering and formatting our [code blocks](/support-center/code-blocks), and CodeMirror provides heaps of themes for you to choose from. The list of themes is available [here](https://codemirror.net/demo/theme.html#default).

## How to Change the Code Theme

To change the code theme, we need to import the theme stylesheet as well as to provide a [setting](/support-center/advanced-settings) to indicate which theme to use.

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
        theme: 'ambiance'
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