---
type: page
title: Hubspot
listed: true
description: 
index_title: Hubspot
hidden: false
keywords: 
tags: 
---

To add Hubspot Analytics integration to %product%, you must have a [plan](https://developerhub.io/pricing) with [Custom HEAD Tags](../custom-javascript.md) enabled.

{% image url="https://image-archive.developerhub.io/image/upload/30375/whcrnufvfv8jrgmhigyn/1590850779.png" width=300 /%}

## Setting up Hubspot Analytics

Follow the steps as provided in [Install the HubSpot tracking code](https://knowledge.hubspot.com/reports/install-the-hubspot-tracking-code#install-the-tracking-code-on-your-website). However, make sure to remove `defer`  and `async` from the script tag.

The script should look like:

{% code %}
```markup {% title="Embed Code" %}
<script type="text/javascript" id="hs-script-loader" src="//js.hs-scripts.com/{{your-id}}.js"></script>
```
{% /code %}

HubSpot Analytics integration is created for traditional websites, while your %product% documentation is built over a single page application. To trigger tracking page views, add the following [Custom HEAD Tag](../custom-javascript.md) after the embed code above:

{% code %}
```markup {% title="Custom HEAD Tag" %}
<script>
	var trackPage = function(event) {
    var _hsq = window._hsq;
		if (!_hsq) {
			console.log('hsq not loaded yet');
			return;
		}
		_hsq.push(['setPath', window.location.pathname]); 
		_hsq.push(['trackPageView']);
	}
	document.addEventListener('onsectionchange', trackPage);
	document.addEventListener('onpagechange', trackPage);
</script>
```
{% /code %}
