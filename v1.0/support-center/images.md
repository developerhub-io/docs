---
type: page
title: Images
listed: true
slug: images
description: 
index_title: Images
hidden: 
keywords: 
tags: blocks
---

You can upload images to your pages by using the Images uploader, or by simply pasting into the page.

On creating the image block, a file dialog to upload an image is shown. After selecting the image, it will be uploaded and served using a CDN (content delivery network) to ensure minimum latency to all of your users.

You can change the image after the upload or delete it using the control icons.

To create an Image:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Image {% icon classes="far fa-images" /%}

## Image Example

An example of an image:

{% image url="https://uploads.developerhub.io/prod/02/mfson8uc57kbxc8i9mfx758je2t0f91sw4kju2g7anvyqlc9f2pprh85whhq0pti.png" caption="Image example" mode="responsive" height="2160" width="3377" %}
{% /image %}

## Image Sizing

Images can be resized by dragging the vertical bar on the right.

## Image Caption

Captions can be added to images which enhances their search-ability on search engines. Simple formatting like the use of bold and italic is possible on captions.

## Image Warnings & Optimisations

If your image is larger than 512 KB in size, then we'll show you a warning that the image is too big. We want your readers to have the best experience, so we want to make sure that you are aware that your images might not be optimised.

Recommended optimisations:

- If the image is a vector, then use SVG.
- If the image is a scalar, then it's best to use JPEG rather than PNG.
- If using JPEG, control the quality. Generally image quality of 85% preserves the quality well while decreasing the size significantly.
- Do not use images greater than 2000px in width.
- For GIFs, attempt to decrease frames per second, size or colour count. You may use an online optimiser such as [Ezgif](https://ezgif.com/optimize).

## Limitations

The file size limit of an image is 10MB.

## FAQ

### Why am I unable to upload an image?

There can be multiple reasons for why the image cannot be uploaded:

- The image is larger than 10MB.
- The file type is not supported. We fully support SVG, JPEG, PNG and GIFs. Other types might still be supported.
- The image is invalid or has an unexpected format. Try to re-create the image, or to save it in another file type using your image viewer.