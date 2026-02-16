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

AI Agent helps editors draft and revise documentation pages by turning a conversation into proposed page edits. It supports similar writing workflows to [AI Writer](/support-center/ai-writer), but it can also search and reference the documentation in your current documentation version to produce more informed, page-specific edit suggestions.

AI Agent never applies changes automatically. Instead, it produces one or more edit suggestions that you can review and apply selectively.

## Who can use AI Agent

AI Agent is available to all editors except reviewers.

AI Agent is enabled when **AI Writer** is enabled. For instructions, see [AI Writer](/support-center/ai-writer).

## Where to find AI Agent

On any page, open the right sidebar and select **AI Agent** {% icon classes="fas fa-robot" /%}

You can modify AI Instructions from **Project Settings** &gt; **AI Features** (at the bottom of the page).

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

## AI Instructions

You can add AI Instructions to control how AI Agent responds. For example, you can ask it to:

- Use a specific language (for example, British English)
- Use a specific tone (for example, friendly and direct, or more formal)
- Follow a style guide (for example, sentence length, preferred terminology, or avoiding jargon)
- Format output in a particular way (for example, what to bold, whether to use lists, or whether to include examples)

If your instructions conflict with each other, AI Agent will do its best to follow the most specific instruction.

{% callout type="info" title="Example instructions" %}
Write in British English. Keep the tone concise and practical. Use short paragraphs and bullet lists. Bold UI labels and button names.
{% /callout %}

## Why use %product%'s AI Agent (vs third-party AI agents)

Using %product%'s AI Agent inside DeveloperHub has practical advantages over using a third-party AI agent to generate documentation edits:

- **Correct page syntax and blocks**: AI Agent is aware of our page syntax and capabilities (including the supported blocks and inline blocks). Third-party agents typically do not have this reference, and may hallucinate blocks or attributes that do not exist.
- **Correct internal links**: AI Agent can link to your documentation pages accurately in the current documentation version. Third-party agents may try to guess links by combining slugs, which can produce broken or incorrect links.

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

## What data is sent to the LLM?

For each question, one or more pages might be sent fully to the LLM.