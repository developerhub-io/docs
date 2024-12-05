---
type: page
title: Videos
listed: true
slug: videos
description: 
index_title: Videos
hidden: 
keywords: 
tags: blocks
---

You can embed videos from many platforms in your documentation pages with our video block.

## Supported Video Platforms

Videos can be embedded natively from:

- Youtube
- Vimeo
- Loom

You can also provide a URL of a video file (Raw).

{% callout type="info" title="Info" %}
You can also embed videos from other providers by using the Custom HTML block.
{% /callout %}

## How to add Videos?

Follow these steps to add a video to your pages:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Video {% icon classes="fas fa-video" /%} 
- Next, choose the provider from the list.
- Paste in the box the URL of the video.

{% image url="https://uploads.developerhub.io/prod/02/9kp06c56w67mbhdanhlb4l4ymadyl0srfbf2urckmp6vhk0g4ifbhj0daidj6wak.png" mode="responsive" height="225" width="674" %}
{% /image %}

- The video will load at once.

## Example Videos

### YouTube

No video is better than old Bohemian Rhapsody music video. Starting the video at a specific time is supported.

{% video %}
{% /video %}

Gotta love that song! 🙌

### Vimeo

Vimeo's interactive video below:

{% video videoId="717779857" provider="vimeo" %}
{% /video %}

### Loom

Loom's own embed video:

{% video videoId="e5b8c04bca094dd8a5507925ab887002" provider="loom" %}
{% /video %}

## Other Video Platforms

To use other video platforms, you can use [auto$](/support-center/custom-html) block to integrate the default browser's HTML5 player.

{% html %}
<video id="preview-player" controls preload="none" width="100%"
     poster="https://media.w3.org/2010/05/sintel/poster.png">
    <source src="https://media.w3.org/2010/05/sintel/trailer.mp4" type="video/mp4"></source>
</video>
{% /html %}

The following HTML would generate this video:

{% code %}
{% tab language="markup" %}
<video id="preview-player" controls preload="none" width="100%"
     poster="http://media.w3.org/2010/05/sintel/poster.png">
    <source src="http://media.w3.org/2010/05/sintel/trailer.mp4" type="video/mp4"></source>
</video>
{% /tab %}
{% /code %}