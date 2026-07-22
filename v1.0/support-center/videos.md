---
type: page
title: Videos
listed: true
description: 
index_title: Videos
hidden: false
keywords: 
tags: blocks
---

With our versatile video block, you can seamlessly embed and upload videos from a variety of platforms into your documentation pages.

## Supported Video Platforms

Videos can be embedded natively from:

- Youtube
- Vimeo
- Loom

You can also provide a URL of a video file (Raw) or upload one.

{% callout title="Info" %}
You can also embed videos from other providers by using the Custom HTML block.
{% /callout %}

## How to add Videos?

Follow these steps to add a video to your pages:

{% synced id="open-block-menu" /%}

- Select Video {% icon classes="fas fa-video" /%}
- Next, choose the provider from the list.
- Paste in the box the URL of the video, or if you chose to upload, select the file.

{% image url="https://uploads.developerhub.io/prod/02/tzlb17s4ayw1rk36grou82hztre8mgdffm3f4a4ldmlpgnpcwnpoxzble262l3as.png" /%}

- The video will load at once.

{% callout title="Max video file size" %}
Video uploads are supported with a maximum file size of 10MB.
{% /callout %}

## Example Videos

### YouTube

No video is better than old Bohemian Rhapsody music video. Starting the video at a specific time is supported.

{% video videoId="fJ9rUzIMcZQ" /%}

Gotta love that song! 🙌

### Vimeo

Vimeo's interactive video below:

{% video provider="vimeo" videoId="717779857" /%}

### Loom

Loom's own embed video:

{% video provider="loom" videoId="e5b8c04bca094dd8a5507925ab887002" /%}

### URL

Embed videos from your own sources with direct links to the video files:

{% video provider="raw" videoId="http://media.w3.org/2010/05/sintel/trailer.mp4?poster=http://media.w3.org/2010/05/sintel/poster.png&preload=none" /%}

You can add search params to the URL to define its options. Here are the attributes which you can use:

{% table layout="auto" %}
{% row %}
{% cell header=true colwidth=[113] %}
Attribute
{% /cell %}
{% cell header=true colwidth=[118] %}
Value Type
{% /cell %}
{% cell header=true %}
Description
{% /cell %}
{% /row %}
{% row %}
{% cell %}
controls
{% /cell %}
{% cell %}
Boolean
{% /cell %}
{% cell %}
Specifies whether the video should have playback controls. Default is true.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
autoplay
{% /cell %}
{% cell %}
Boolean
{% /cell %}
{% cell %}
Indicates that the video will start playing automatically.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
loop
{% /cell %}
{% cell %}
Boolean
{% /cell %}
{% cell %}
Indicates that the video will start over again, when finished.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
muted
{% /cell %}
{% cell %}
Boolean
{% /cell %}
{% cell %}
Specifies that the video should be muted by default.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
playsinline
{% /cell %}
{% cell %}
Boolean
{% /cell %}
{% cell %}
Indicates if the video is to be played inline.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
preload
{% /cell %}
{% cell %}
String
{% /cell %}
{% cell %}
Hints to the browser about whether to preload the video (auto, metadata, none).
{% /cell %}
{% /row %}
{% row %}
{% cell %}
poster
{% /cell %}
{% cell %}
URL
{% /cell %}
{% cell %}
The URL of an image to show while the video is downloading or until the user hits the play button.
{% /cell %}
{% /row %}
{% /table %}

For example: `https://example.com/video.mp4?autoplay=true&loop=true&muted=true&playsinline=true&controls=false` to play the video inline.

## Other Video Platforms

To use other video platforms, you can use [Custom HTML](custom-html.md) block to embed the video.
