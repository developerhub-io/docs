---
type: page
title: Previewing Documentation
listed: true
description: 
index_title: Previewing Documentation
hidden: false
keywords: 
tags: 
---

%product% was designed to unify the view between the editor and the live version.

There is no need to preview your documentation. The editor already is showing you the same view of how it will look to your documentation readers 😉

{% callout type="success" title="Woah!" %}
What was I thinking before?!
{% /callout %}

If you are really keen on previewing it, then you can see it live by publishing it.

## URL Strategy

URL, which is the link you see in your browser, defines which project, version and section (documentation or API reference) are loaded.

Here is a summary of how we load resources using URLs:

{% table layout="auto" %}
{% row %}
{% cell header=true colwidth=[388] %}
URL
{% /cell %}
{% cell header=true %}
Result
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<section>`
{% /cell %}
{% cell %}
Loads the default page in the specified documentation, or the specified API reference in the default version.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<documentation>/<page>`
{% /cell %}
{% cell %}
Loads the page in the specified documentation in the default version
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<version>/<section>`
{% /cell %}
{% cell %}
Loads the default page in the specified documentation, or the specified API reference in the specified version
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<version>/<documentation>/<page>`
{% /cell %}
{% cell %}
Loads the specified page in the specified documentation in the specified version
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/`
{% /cell %}
{% cell %}
Loads the landing page if enabled, or the default page in the default section of the default version
{% /cell %}
{% /row %}
{% /table %}

The following are deprecated URLs which you should not use anymore, however they are now redirected for backward-compatibility:

{% table layout="auto" %}
{% row %}
{% cell header=true %}
URL
{% /cell %}
{% cell header=true %}
Redirected To
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<version>/-/-`
{% /cell %}
{% cell %}
`https://<project>/<version>/<documentation>`
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<version>/<documentation>/-`
{% /cell %}
{% cell %}
`https://<project>/<version>/<documentation>`
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<reference>/ref`
{% /cell %}
{% cell %}
`https://<project>/<reference>`
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/<version>/<reference>/ref`
{% /cell %}
{% cell %}
`https://<project>/<version>/<reference>`
{% /cell %}
{% /row %}
{% row %}
{% cell %}
`https://<project>/-/-/-`
{% /cell %}
{% cell %}
`https://<project>/<section>`
{% /cell %}
{% /row %}
{% /table %}

Any other form of link will load the default page.

Note that you can add a base path if you are [hosting under your own existing website](hosting.md#hosting-under-your-own-custom-domain), the above rules would still be applicable but a base path would be added right after the `<project>`. For example, instead of `https://<project>/<version>/<documentation>/<page>`, the link would be `https://<project>/<base-path>/<version>/<documentation>/<page>`.

## Print-Optimised

Our pages are print-optimised (specially for A4 paper size). We recommend having the wide documentation layout when printing, and always printing from the published documentation site (not on the editor). If you are an enterprise customer, then you may also [export an entire version as PDF](pdf-export.md).

{% image url="https://image-archive.developerhub.io/image/upload/285/eyb5rboboeyujowo73rl/1549534333.jpg" /%}

## Embed Mode

%product% sites can be embedded using `iframe` as needed. This is specially helpful if you wish to create a documentation widget so your reader can follow the instructions without leaving their tabs.

There are two types of embed mode:

- Minimal: Hides the top navigation, footer, index and table of contents. Mode is `embed`.
- Normal: Hides the top navigation and footer only. Mode is `embed_full`.

{% callout title="Note" %}
Minimal and normal modes are the same when window width is small as index and table of contents are hidden when window width is small by default.
{% /callout %}

Embed mode is enabled by adding a `?mode=embed` or `?mode=embed_full` to any %product% URL (except landing pages). For example, if you want to show your users a page under `https://dev.company.io/ios/getting-started` then you may load an `iframe` with `src="https://dev.company.io/ios/getting-started?mode=embed"`

{% code %}
```markup {% title="HTML" %}
<iframe style="position:fixed;width: 500px;height: 450px;background: white;right: 100px;bottom: 0px;z-index: 10;border: 1px solid #bbb;border-radius: 5px;" src="https://docs.developerhub.io/support-center/uploading-references?mode=embed"></iframe>
```
{% /code %}

Here is a preview:

{% image url="https://image-archive.developerhub.io/image/upload/285/x76hvvut9jyurqhueneg/1610123546.png" /%}
