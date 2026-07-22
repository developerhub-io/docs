---
type: page
title: Zendesk Widget
listed: true
description: 
index_title: Zendesk Widget
hidden: false
keywords: 
tags: 
---

To add Zendesk Web Widget integration to %product%, you must have a [plan](https://developerhub.io/pricing) with [Custom HEAD Tags](../custom-javascript.md) enabled.

{% image url="https://uploads.developerhub.io/prod/02/zkmmo5ydr7dkvau0f6oxczi2x4qlloc4ngseyrdrmdftzyfv7zbnu35bs1r5r4v4.png" /%}

## Setting up Zendesk Web Widget

Follow the steps as provided in [Quickstart - Web Widget (Classic) APIs](https://developer.zendesk.com/documentation/classic-web-widget-sdks/web-widget/quickstart-tutorials/web-widget-javascript-apis/). Add the following [Custom HEAD Tag](../custom-javascript.md) replacing `YOUR_SNIPPET_KEY` with your own key:

{% code %}
```markup {% title="Custom HEAD Tag" %}
<!-- Start of Zendesk Widget script -->
<script id="ze-snippet" src="https://static.zdassets.com/ekr/snippet.js?key=YOUR_SNIPPET_KEY">
</script>
<!-- End of Zendesk Widget script -->
```
{% /code %}
