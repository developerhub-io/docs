---
type: page
title: Zendesk Widget
listed: true
slug: zendesk-integration
description: 
index_title: Zendesk Widget
hidden: 
keywords: 
tags: 
---

To add Zendesk Web Widget integration to %product%, you must have a [plan](https://developerhub.io/pricing) with [auto$](/support-center/custom-javascript) enabled.

{% image url="https://uploads.developerhub.io/prod/02/zkmmo5ydr7dkvau0f6oxczi2x4qlloc4ngseyrdrmdftzyfv7zbnu35bs1r5r4v4.png" mode="responsive" height="344" width="516" %}
{% /image %}

## Setting up Zendesk Web Widget

Follow the steps as provided in [Quickstart - Web Widget (Classic) APIs](https://developer.zendesk.com/documentation/classic-web-widget-sdks/web-widget/quickstart-tutorials/web-widget-javascript-apis/). Add the following [Custom HEAD Tag](/support-center/custom-javascript) replacing `YOUR_SNIPPET_KEY` with your own key:

{% code %}
{% tab language="markup" title="Custom HEAD Tag" %}
<!-- Start of Zendesk Widget script -->
<script id="ze-snippet" src="https://static.zdassets.com/ekr/snippet.js?key=YOUR_SNIPPET_KEY">
</script>
<!-- End of Zendesk Widget script -->
{% /tab %}
{% /code %}