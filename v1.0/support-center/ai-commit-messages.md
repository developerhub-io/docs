---
type: page
title: AI Commit Messages
listed: true
slug: ai-commit-messages
description: 
index_title: AI Commit Messages
hidden: 
keywords: 
tags: ai
---

In %product%, AI can automatically annotate the history of every page, making it easier for you to track and understand the changes and activities that have taken place.

{% callout type="warning" title="Beta" %}
This is a beta feature. Your [feedback](/support-center/contact-us) is appreciated.
{% /callout %}

{% image url="https://uploads.developerhub.io/prod/02/pcjj39ox3jnxt5bfwigtexxrenlz172ha8kzz8zfdb81fjodtt3rjwh1xdbohxgy.png" mode="responsive" height="902" width="828" %}
{% /image %}

## Enabling AI Commit Messages

AI commit messages are disabled by default and must be enabled by an admin. To enable AI commit messages:

- Open Project Settings → **AI Features**.
- Check **AI Commit Messages**.
- Click **Save changes** in the top menu.

Every content change will have its page history annotated by AI.

## What data is sent to OpenAI?

The page content diff is sent to OpenAI when AI annotates page histories.