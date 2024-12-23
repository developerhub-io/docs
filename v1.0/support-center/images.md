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

A photo of a kitty:

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1539371521/11/ma6fngctzdw4pcfc7urk.jpg" caption="Image example" mode="responsive" height="1200" width="1920" %}
{% /image %}

Cute right? 😍

## Image Sizing

Uploaded images can be shown to your readers in four different sizes:

1. Small size {% icon classes="fas fa-compress" /%}
2. Big size {% icon classes="fas fa-expand" /%}
3. Responsive size {% icon classes="fas fa-desktop" /%}
4. Full width size {% icon classes="fas fa-arrows-alt-h" /%}

The size can be selected in the editor per image using the image controls.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1561510159/11/yumibayzcdzdupyik4sp.jpg" caption="Image sizing" mode="responsive" height="928" width="1672" %}
{% /image %}

### Responsive Size

Responsive size ensures that the size of the image is responsive to the screen pixel ratio. This allows for crisper images on Retina display and any high resolution display.

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