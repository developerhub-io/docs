---
type: page
title: Quick Switcher
listed: true
slug: quick-switcher
description: 
index_title: Quick Switcher
hidden: 
keywords: 
tags: 
---

As your documentation grows in size, finding the pages through a long index becomes harder. Quick switcher helps you find content easier.

Quick switcher is able to perform the following:

- **Find Page**: Search for a page or an API reference by title or slug (case insensitive).
- **Find Text**: Search for text in pages only (case insensitive).
- **Find & Replace**: Finds text in pages and replaces it (case sensitive).

{% callout type="info" title="Info" %}
This is only available in the editor. Your readers can use the global search directly.
{% /callout %}

## How to open Quick Switcher

To open quick switcher, click on the search bar or hit `⌘/Ctrl + K`  or the search icon {% icon classes="fas fa-search inv-icon" /%} in the bottom right corner. Type in your search and hit enter to choose best result.

## Search Mode: Find Page

Find page searches through all pages and API references by title and slug in the version you're on. Typo-tolerance search is used here.

{% image url="https://uploads.developerhub.io/prod/02/cm553rjpauugjnf9llv5pmj0tbnhpv4xw5536k0aezno815pcuic6sc1xaczxyvi.png" mode="responsive" height="1070" width="2150" %}
{% /image %}

## Search Mode: Find Text

Find text searches through all pages in the version you're on for text. Search is performed on [Darkdown](/support-center/exporting-documentation#darkdown) format and is not case sensitive.

{% image url="https://uploads.developerhub.io/prod/02/jf6o54rxx3rf5agijr6cbrsqcysjs8bxljwi6mir7m6xb1sv1oj6691oien51ofm.png" mode="responsive" height="1064" width="2074" %}
{% /image %}

## Search Mode: Find & Replace

Find & replace searches through all pages in the version you're on for text, and allows you to replace the text directly. Search is performed on [Darkdown](/support-center/exporting-documentation#darkdown) format and is case sensitive.

All occurrences that can be replaced would be shown to you prior to replacing them.

{% image url="https://uploads.developerhub.io/prod/02/nye3lm5949pscetd8kacvanhayhxhjy6cjgfrrumum3au25kt8xlksvgwztifo2o.png" mode="responsive" height="1072" width="1758" %}
{% /image %}

{% callout type="warning" title="Warning" %}
Once text is replaced, there is no way to undo the operation. Check all occurrences and verify that you wish for ALL occurrences to be replaced before continuing.
{% /callout %}

## Notes about Quick Switcher

Find Text and Find & Replace search through [Darkdown](/support-center/exporting-documentation#darkdown) format, with this come a few notes:

- Search performed is exact text search. This means that it is not typo tolerant.
- To search in formatted text like "pied **piper**", you'd need to search for `pied **piper**`. Searching for `pied piper` will not yield results.
- Text in [blocks](/support-center/blocks) is also searched. Text in [auto$](/support-center/custom-html) and [auto$](/support-center/synced-blocks) among other dynamic blocks is not searched.
- Text in links is not searched.
- Text in [inline blocks](/support-center/blocks#inline-blocks) is not searched.