---
type: page
title: Markdoc Format
listed: true
description: 
index_title: Markdoc Format
hidden: false
keywords: 
tags: 
---

Markdoc format is the format used when pages are synced on %product% using [GitHub Sync](../github-sync.md). Markdoc is markdown-based authoring framework for writing documentation.

If you author pages with an AI coding agent, our [Markdoc Agent Skill](write-markdoc-with-ai.md) teaches it this exact syntax, so its edits round-trip cleanly.

## Frontmatter Syntax

Every page has a frontmatter header, such as this one:

{% code %}
```markup {% title="Frontmatter" %}
---
type: page
title: Getting Started
listed: true
slug: getting-started
description: 
index_title: Getting Started
hidden: false
keywords: keyword1,keyword2
tags: tag1,tag2
---
```
{% /code %}

## Markdoc Syntax

Markdoc is a superset of Markdown, so you can still write Markdown as you usually do, including the following nodes:

{% code %}
````markdown
## Headers

**Bold**

_Italic_

[Links](/docs/nodes)

![Images](/logo.svg)

Unordered Lists
- Item 1
- Item 2
- Item 3

Ordered Lists
1. Item 1
2. Item 2
	1. Item 1 under 2
3. Item 3

> Callouts

`Inline code`

```
Code fences
```
````
{% /code %}

In addition to Markdown, we provide tags and attributes for all [blocks](../writing-documentation/blocks.md) and inline blocks.

Blocks have the following syntax:

{% code %}
```markdown
{% block-type attr1="value1" attr2="value" %}
contents
{% /block-type %}
```
{% /code %}

While inline blocks have the following syntax:

{% code %}
```markdown
{% icon classes="fas fa-bookmark" /%}
{% glossary term="CDN" /%}
```
{% /code %}

The syntax is shown below for every block with an example:

### Code Block

A **Code block** is a single fenced block with the language on the opening fence. **Code tabs** wrap several fenced blocks in a `{% code %}` / `{% /code %}` pair.

{% code %}
````markdown
```javascript {% title="fibonacci.js" %}
function fibonacci(num, memo) {
  memo = memo || {};

  if (memo[num]) return memo[num];
  if (num <= 1) return 1;

  return memo[num] = fibonacci(num - 1, memo) + fibonacci(num - 2, memo);
}
```
````
{% /code %}

### Images

Self-closing when there is no caption, or a body form when there is:

{% code %}
```markdown
{% image url="https://uploads.developerhub.io/dev/V5Na/u0dpegq8xdpnclhctkpxycekhj04sev9j2kztstph3bnj41cde13o7vuzlpxw6yj.jpg" width=464 %}
Image caption
{% /image %}
```
{% /code %}

### Tables

Tables are `{% row %}` and `{% cell %}` trees; a header cell sets `header=true`. A simple table can also be written as a plain Markdown pipe table.

{% code %}
```markdown
{% table layout="auto" %}
{% row %}
{% cell header=true %}
Parameter
{% /cell %}
{% cell header=true %}
Type
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user_id
{% /cell %}
{% cell %}
int
{% /cell %}
{% /row %}
{% /table %}
```
{% /code %}

### Callouts

{% code %}
```markdown
{% callout type="success" title="Success" %}
Great **success**!
{% /callout %}
```
{% /code %}

### Videos

{% code %}
```markdown
{% video provider="loom" videoId="e5b8c04bca094dd8a5507925ab887002" /%}
```
{% /code %}

### Synced Blocks

{% code %}
```markdown
{% synced id="open-block-menu" /%}
```
{% /code %}

### Custom HTML

{% code %}
```markdown
{% html %}
SWISHHTMLBODY0
{% /html %}
```
{% /code %}

### Tabs

{% code %}
```markdown
{% tabs %}
{% tab title="Android" %}
Android content.
{% /tab %}
{% tab title="iOS" %}
iOS content.
{% /tab %}
{% /tabs %}
```
{% /code %}

### Changelog

{% code %}
```markdown
{% changelog label="31 July 2024" slug="31-july-2024" date="2024-07-31" %}
- {% badge type="warning" text="Change" /%} **API References**: Writers can [create and edit](/support-center/collaboration) API references in draft now.
{% /changelog %}
```
{% /code %}

### GitHub Code

{% code %}
```markdown
{% github-code url="https://github.com/torvalds/linux/blob/master/kernel/signal.c#L152-L170" /%}
```
{% /code %}

### Index List

{% code %}
```markdown
{% index-list /%}
```
{% /code %}
