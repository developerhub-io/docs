---
type: page
title: Inline Images
listed: true
slug: inline-images
description: 
index_title: Inline Images
hidden: 
keywords: 
tags: inline-blocks
---

{% callout type="warning" title="Beta" %}
This is a beta feature. Your [feedback](/support-center/contact-us) is appreciated.
{% /callout %}

Inline images are images that you can add inside tables, callouts, or anywhere.

## How to add an Inline Image?

To add an inline image, start typing "/" and choose **Image** from the inline block list.

Also, if you paste an image inside a table, it will be created as an inline image directly.

## Inline Image Modes

Inline images support two modes which you can modify by clicking on the image and selecting one. The modes are:

- Fit width: The image would take the maximum the entire width of the container. If the image's natural width is smaller than the container, it would take the natural width. An image pasted into a table would by default have this mode.
- Resizable: The image can be resized, but it cannot be made larger than its natural size.

## Inline Image Examples

{% table widths="173,0" %}
| Type of Animal | Sound | How it looks like | 
| ---- | ---- | ---- | 
| Cat | Meow | {% inline-image url="https:\\/\\/uploads.developerhub.io\\/prod\\/02\\/kgnzg0ig37q5lyjn3sxwjekoxmvcio2qf4s1sutk77z61157kyih40xtxrj7p05l.png" width="113" /%} | 
| Dog | Woof | {% inline-image url="https:\\/\\/uploads.developerhub.io\\/prod\\/02\\/o4y7fb9jve2gbw4zdq1j3p5b5txg9aio7vymkjrnle44j8fcsizrccj3nd0oo9o3.png" width="88" /%} | 
{% /table %}