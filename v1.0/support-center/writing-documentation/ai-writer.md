---
type: page
title: AI Writing Tools
listed: true
description: 
index_title: AI Writing Tools
hidden: false
keywords: 
tags: ai
---

{% callout title="Info" %}
The following page was written partly by AI Writing Tools.
{% /callout %}

AI Writing Tools assist you with routine writing tasks and content brainstorming. Whether you're looking to refine your text, enhance readability, or generate new ideas, they can help streamline the process efficiently.

Formerly called AI Writer.

{% video provider="raw" videoId="https://uploads.developerhub.io/prod/02/z8xlri6ihst36627hnbt10vbvv22z1sfxmnsij4p04hj1hov1wtsx8e84usya19l.mp4" /%}

## AI Writing Tools features

Select text in the editor, then pick a function from the **AI** button at the left of the toolbar. You can:

- **Simplify text**: Make complex sentences easier to read and understand.
- **Enhance**: Improve overall writing quality, making text more engaging and polished.
- **Fix spelling \& grammar**: Automatically correct errors to improve clarity and professionalism.
- **Make text shorter**: Condense lengthy content while retaining key information.
- **Expand**: Expand on ideas and provide more detailed explanations.
- **Insert emojis**: Add relevant emojis to make your text more engaging and expressive.
- **Autocomplete text**: Generate suggested completions to speed up writing.

## Enabling AI Writing Tools

AI Writing Tools are disabled by default and must be enabled by an admin. To enable them:

- Open Project Settings → **AI** → **AI Agents \& MCP**, then the **Editor** tab.
- Under **Writing**, turn on **AI in the editor**.
- Click **Save changes** in the top menu.
- Refresh the page for changes to apply.

**AI in the editor** is a single switch over every AI that works on your docs, so it turns on [AI Agent](../ai-agent.md) at the same time.

## Using AI Writing Tools

AI Writing Tools stream their response straight into the page, shown in a distinct colour while they work. When a function finishes, a small bar gives you three choices:

- **Apply**: accept the suggestion and replace your original text.
- **Try again**: run the same function again for a different result.
- **Discard**: dismiss the suggestion and keep your original text.

Nothing is changed until you click **Apply**, so you stay in full control of your content.

## AI Writing Tools Limitations

- Output tokens are limited. This may result in incomplete responses being displayed.
- Text formatting (including variables, glossary or any rich text features) might not be preserved in certain cases.
- Rewriting a selection always runs on a small fast model. The [agent model](../ai-features.md#which-models-we-use) an admin picks for the project does not apply here.

## What data is sent to the LLM?

Only selected text is sent to the LLM when an AI Writing Tool is used.
