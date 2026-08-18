---
type: page
title: Frequently Asked Questions (FAQ)
listed: true
description: 
index_title: Frequently Asked Questions (FAQ)
hidden: false
keywords: 
tags: 
---

{% accordion-group %}
{% accordion title="What is it?" %}
%product% is an agentic documentation platform. It is a managed service for writing, publishing and reviewing customer-facing docs, made up of user guides and API references. Attach your code repository and an [agent](ai-agent.md) drafts the changes your pull requests imply, for someone on your team to review before anything publishes.
{% /accordion %}

{% accordion title="Is it a CMS?" %}
Yes, %product% is a content management system (CMS) for documentation.
{% /accordion %}

{% accordion title="What is a documentation?" %}
Documentation is an unlimited amount of pages that are correlated, grouped together and are shown on one index. For example, this support centre which you are currently viewing is only one documentation. See [project structure](project-structure.md) for more information.
{% /accordion %}

{% accordion title="How can my users view my documentation pages?" %}
They can navigate to your own documentation pages through a subdomain that you assign under %product% domain or through a subdomain under your own existing domain. Your docs can also be hosted on a path under your existing domain.

For example, that could be: `pied-piper.developerhub.io` or `docs.your-company.com`, or even `your-company.com/docs`. See the [other hosting options here](hosting.md).
{% /accordion %}

{% accordion title="Can I use my own custom domain?" %}
Yes. See [Using Custom Domain](hosting/using-custom-domain.md).
{% /accordion %}

{% accordion title="Can I restrict who can view the documentation?" %}
We provide many ways for making your docs site private, see [all privacy options](private-docs.md),
{% /accordion %}

{% accordion title="Can I restrict access to certain documentation/pages?" %}
Our projects can either be public or private at a time. If you are restricting access internally to your teammates, then they can already access it through the editor. If you want to restrict access for readers who do not have %product% teammate access, then you would need a second project that is [protected/private](private-docs.md).
{% /accordion %}

{% accordion title="Is there support for draft versions?" %}
Each version can be published or unpublished. Unpublished versions are the equivalent of draft versions.
{% /accordion %}

{% accordion title="How do the docs get hosted?" %}
We handle all the hosting. Check out all [hosting options here](hosting.md).
{% /accordion %}

{% accordion title="Is it mobile friendly?" %}
Yes, all the published pages are optimised for mobile viewing. The editor has only been tested for use on desktop or iPad, however.
{% /accordion %}

{% accordion title="Can I change how it looks?" %}
Every bit and piece can be changed. We provide [many built-in options](customising-visuals.md) to make it easy for you to change logos, colours, navigation, font and layout. You can also provide your own [Custom Landing Page](landing-page/custom-landing-page.md), [Custom CSS](customising-visuals/custom-css.md), [Custom HEAD Tags](custom-javascript.md) and [Custom Footer](customising-visuals/custom-footer.md).
{% /accordion %}

{% accordion title="Would search engines index the pages?" %}
If your project is public, then by default search engines will be able to index all the published pages. You can change this from the [project settings](seo.md#do-not-want-to-be-visible).
{% /accordion %}

{% accordion title="Accented characters are not showing properly, what can I do?" %}
That could happen because of our default font, change the project font to a font that supports your language.
{% /accordion %}

{% accordion title="Do you support DITA or DocBook?" %}
There is no support for XML content models. %product% provides a modern experience with a WYSIWYG editor and advanced features for formatting, linking, data import/export and customisation.
{% /accordion %}

{% accordion title="Do you support Single-Sourcing?" %}
Yes, we support [content reuse](synced-blocks.md) and [templates](templates.md).
{% /accordion %}

{% accordion title="Do you support file uploads/attachments?" %}
We have native support for [image](images.md) and [video](videos.md) uploads. Video uploads have a maximum file size of 10MB; for anything larger, upload the video to YouTube (or any other provider) and show it using a [video block](videos.md), or embed it using a [custom HTML block](custom-html.md). For other file uploads, you would need to upload the file to a hosting provider (such as your own S3 bucket), and then you may add a link in your documentation page or even create a [nice download button](custom-html.md#fancy-button) for it.
{% /accordion %}

{% accordion title="Can we sync the docs with a GIT repo?" %}
Yes, check [GitHub Sync](github-sync.md) which allows you to set up two-way sync between GitHub and %product%.
{% /accordion %}

{% accordion title="Do you support GraphQL docs?" %}
Yes. Check [GraphQL](integrations/graphql.md) where you can embed it in a [Custom HTML](custom-html.md) block or in an entire [landing page](landing-page.md).
{% /accordion %}

{% accordion title="Do you support ChatGPT chat-like experience for search?" %}
Yes, check [AI Assistant](writing-documentation/ai-search.md).
{% /accordion %}

{% accordion title="Do you support AsyncAPI references?" %}
Not at the moment. If you'd like to work with us on an implementation, please [contact us](contact-us.md).
{% /accordion %}

{% accordion title="Are there public examples of documentation built with %product%?" %}
Yes, see the [customers section on our pricing page](https://developerhub.io/pricing#customers) for a selection of live documentation portals built with %product%.
{% /accordion %}
{% /accordion-group %}

## Got Other Questions?

We'd love it if you [contact](contact-us.md) us!
