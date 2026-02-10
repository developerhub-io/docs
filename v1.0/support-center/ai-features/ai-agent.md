---
type: page
title: AI Agent
listed: true
slug: ai-agent
description: 
index_title: AI Agent
hidden: 
keywords: 
tags: 
---

AI Agent helps editors draft and revise documentation pages by turning a conversation into proposed page edits. Like [AI Writer](/support-center/ai-writer), it can help you write. Unlike [AI Writer](/support-center/ai-writer), AI Agent can search and reference the documentation in your current documentation version to produce more informed, page-specific edit suggestions.

AI Agent never applies changes automatically. Instead, it produces one or more edit suggestions that you can review and apply selectively.

## Who can use AI Agent

AI Agent is available to all editors except reviewers.

AI Agent is enabled when **AI Writer** is enabled. For instructions, see [AI Writer](/support-center/ai-writer).

## Where to find AI Agent

On any page, open the right sidebar and select **AI Agent** {% icon classes="fas fa-robot" /%}

## What AI Agent can do

AI Agent can help you:

- Draft new pages
- Revise or rewrite existing text
- Generate summaries
- Plan content (for example, outlines and section suggestions)
- Restructure a page (for example, reorder sections and improve flow)

AI Agent returns changes as edit suggestions that can include structured blocks. It handles blocks automatically when proposing edits.

## How AI Agent works

AI Agent can use documentation context to produce better edits:

- It can access the **current page** you are editing.
- It can search the **same version** you are currently viewing.
- Search includes all content in that version, including drafts and unpublished pages.

AI Agent produces proposed edits that are scoped to a page. You can apply any suggestion that you want, and skip the rest.

## Applying edit suggestions

When AI Agent provides edit suggestions, you can:

- Select **Apply** on a suggestion to apply it to the page
- Apply suggestions selectively (you do not need to apply all suggestions)

Applied suggestions update the page in [draft mode](/support-center/draft-mode):

- Applying a suggestion updates the draft content on the page.
- The draft is **not saved automatically**.
- You can review and edit further before saving or publishing.

## Privacy

Conversations with AI Agent are personal and are scoped to the page.

## AI Agent vs AI Writer

AI Agent and AI Writer both help with writing and editing, but they are designed for different workflows.

{% table widths="" %}
| Feature | AI Writer | AI Agent | 
| ---- | ---- | ---- | 
| Where you use it | Inline while editing | From the right sidebar on a page | 
| Primary interaction | Inline assistance | Conversational workflow that produces edit suggestions | 
| Access to documentation context | Only highlighted text | Can search and reference documentation in the current version, including drafts and unpublished content | 
| Output | Writing assistance inline | One or more edit suggestions you can apply selectively | 
| Applies changes automatically | Yes | No | 
{% /table %}

## Notes and limitations

- AI Agent cannot modify page info (slug, description, etc...).
- AI Agent cannot generate images.