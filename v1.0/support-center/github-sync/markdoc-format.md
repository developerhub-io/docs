---
type: page
title: Markdoc Format
listed: true
slug: markdoc-format
description: 
index_title: Markdoc Format
hidden: 
keywords: 
tags: 
---

Markdoc format is the format used when pages are synced on %product% using [auto$](/support-center/github-sync). Markdoc is markdown-based authoring framework for writing documentation.

## Frontmatter Syntax

Every page has a frontmatter header, such as this one:

{% code %}
{% tab language="markup" title="Frontmatter" %}
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
{% /tab %}
{% /code %}

## Markdoc Syntax

Markdoc is a superset of Markdown, so you can still write Markdown as you usually do, including the following nodes:

{% code %}
{% tab language="markdown" %}
## Headers

**Bold**

_Italic_

[Links](/docs/nodes)

![Images](/logo.svg)

Lists
- Item 1
- Item 1
- Item 1

> Callouts

`Inline code`

```
Code fences
```
{% /tab %}
{% /code %}

In addition to Markdown, we provide tags and attributes for all [blocks](/support-center/blocks) and inline blocks.

Blocks have the following syntax:

{% code %}
{% tab language="markdown" %}
{% block-type attr1="value1" attr2="value" %}
contents
{% /block-type %}
{% /tab %}
{% /code %}

While inline blocks have the following syntax:

{% code %}
{% tab language="markdown" %}
{% block-type attr1="value1" attr2="value2" /%}
{% /tab %}
{% /code %}

The syntax is shown below for every block with an example:

### Code Block

{% code %}
{% tab language="markdown" %}
{% code %}
{% tab language="javascript" %}
function fibonacci(num, memo) {
  memo = memo || {};

  if (memo[num]) return memo[num];
  if (num <= 1) return 1;

  return memo[num] = fibonacci(num - 1, memo) + fibonacci(num - 2, memo);
}
{% /tab %}
{% /code %}
{% /tab %}
{% /code %}

### Images

{% code %}
{% tab language="markdown" %}
{% image url="https://uploads.developerhub.io/dev/V5Na/u0dpegq8xdpnclhctkpxycekhj04sev9j2kztstph3bnj41cde13o7vuzlpxw6yj.jpg" caption="Image example" mode="responsive" height="1200" width="1920" %}
{% /image %}
{% /tab %}
{% /code %}

### Tables

{% code %}
{% tab language="markdown" %}
{% table widths="null,100" %}
| Parameter | Type | Default Value | 
| ---- | ---- | ---- | 
| user_id | int | Auto generated | 
| user_name | string | John Doe | 
| user_age | int | 25 | 
{% /table %}
{% /tab %}
{% /code %}

### Callouts

{% code %}
{% tab language="markdown" %}
{% callout type="success" title="Success" %}
Great **success**!
{% /callout %}
{% /tab %}
{% /code %}

### Videos

{% code %}
{% tab language="markdown" %}
{% video videoId="e5b8c04bca094dd8a5507925ab887002" provider="loom" %}
{% /video %}
{% /tab %}
{% /code %}

### Synced Blocks

{% code %}
{% tab language="markdown" %}
{% synced id="open-block-menu" %}
{% /synced %}
{% /tab %}
{% /code %}

### Custom HTML

{% code %}
{% tab language="markdown" %}
{% html %}
<a href="https://docs.developerhub.io/?goto=wide" target="_blank" style="background-color: #333; color: white; padding: 12px; border-radius: 3px; text-decoration: none !important">
    See Wide Layout
</a>
{% /html %}
{% /tab %}
{% /code %}

### Tabs

{% code %}
{% tab language="markdown" %}
{% tabs %}
{% tab title="Android" %}
Android Tab
{% /tab %}
{% tab title="iOS" %}
iOS Tab
{% /tab %}
{% /tabs %}
{% /tab %}
{% /code %}

### GitHub Code

{% code %}
{% tab language="markdown" %}
{% github-code url="https://github.com/torvalds/linux/blob/master/kernel/signal.c#L152-L170" %}
{% /github-code %}
{% /tab %}
{% /code %}

### Index List

{% code %}
{% tab language="markdown" %}
{% index-list %}
{% /index-list %}
{% /tab %}
{% /code %}

### Inline Blocks

{% code %}
{% tab language="markdown" %}
Variables: %user.id%
Badges: {% badge type="success" text="Great" /%}
Icons: {% icon classes="layers" /%}
Keyboard Keys: {% key key="F" /%}
Glossary: {% glossary term="product" /%}
Inline Images: {% inline-image url="https://img.com/img.url" width="100" /%}
{% /tab %}
{% /code %}