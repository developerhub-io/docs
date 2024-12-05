---
type: page
title: GitHub Code
listed: true
slug: github-code
description: 
index_title: GitHub Code
hidden: 
keywords: 
tags: blocks
---

Embed code from GitHub repository right into %product%. This allows you to keep code in the docs synced with changes in the repository.

To create GitHub Code block:

{% synced id="open-block-menu" %}
{% /synced %}

- Select GitHub Code {% icon classes="fab fa-github" /%}.
- Paste in the box the URL of the GitHub file, for example: `https://github.com/torvalds/linux/blob/master/kernel/signal.c`.

You can also only embed a few lines by selecting the lines on GitHub, such a URL would show: `https://github.com/torvalds/linux/blob/master/kernel/signal.c#L15-L29`.

The file selected will be rendered as:

- Markdown if the file name ends in `.md`.
- Jupyter notebook if the file name ends in `.ipynb`.
- Raw file otherwise.

Embedding is powered by [https://emgithub.com/](https://emgithub.com/). You can change the code theme using [advanced settings](/support-center/advanced-settings) by modifying `code.githubTheme`.

## Example GitHub Code

Source: `https://github.com/torvalds/linux/blob/master/kernel/signal.c#L152-L170`.

{% github-code url="https://github.com/torvalds/linux/blob/master/kernel/signal.c#L152-L170" %}
{% /github-code %}