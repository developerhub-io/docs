---
type: page
title: llms.txt
listed: true
slug: llms-txt
description: 
index_title: llms.txt
hidden: 
keywords: 
tags: 
---

{% callout type="warning" title="Beta" %}
This is a beta feature. Your [feedback](/support-center/contact-us) is appreciated.
{% /callout %}

The file named `llms.txt`, located at the base of your project path, is integral for enabling large language models (LLMs) to effectively process and understand your documentation. It's the equivalent of your docs but its intended audience is a computer rather than a human. `llms.txt` is generated using a standard format from your docs.

## Enabling llms.txt

`llms.txt` support is disabled by default and must be enabled by an admin. To enable `llms.txt`:

- From the left sidebar, open **Project Settings** {% icon classes="fas fa-layer-group" /%} 
- Under **AI**, check **Enable llms.txt**.

`llms.txt` file can be found at the base of your project.

For projects without a basepath: `https://<project-url>/llms.txt`.

For projects with a basepath: `https://<project-url>/<basepath>/llms.txt`.

{% callout type="info" title="Info" %}
`llms.txt` is updated every 6 hours
{% /callout %}

## Markdown for LLMs

When llms.txt is enabled, pages are also readable in markdown format if `.md` is added to the end of a URL. For example, if you visit this page with `.md` added to the end of its URL, then you can read its markdown equivalent.

[https://docs.developerhub.io/support-center/llms-txt.md](https://docs.developerhub.io/support-center/llms-txt.md)

## Limitations of llms.txt support

- We only support `llms.txt` for now. `llms-full.txt` is not supported yet.