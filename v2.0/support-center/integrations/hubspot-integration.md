---
type: page
title: Hubspot
listed: true
slug: hubspot-integration
description: 
index_title: Hubspot
hidden: 
keywords: 
tags: 
---

To add Hubspot Analytics integration to %product%, you must have a [plan](https://developerhub.io/pricing) with [](/support-center/custom-javascript) enabled.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1590850779/30375/whcrnufvfv8jrgmhigyn.png" mode="300" height="315" width="841" %}
{% /image %}

## Setting up Hubspot Analytics

Follow the steps as provided in [Install the HubSpot tracking code](https://knowledge.hubspot.com/reports/install-the-hubspot-tracking-code#install-the-tracking-code-on-your-website). However, make sure to remove `defer`  and `async` from the script tag.

The script should look like:

{% code %}
{% tab language="markup" title="Embed Code" %}
<script type="text/javascript" id="hs-script-loader" src="//js.hs-scripts.com/{{your-id}}.js"></script>
{% /tab %}
{% /code %}

HubSpot Analytics integration is created for traditional websites, while your %product% documentation is built over a single page application. To trigger tracking page views, add the following [Custom HEAD Tag](/support-center/custom-javascript) after the embed code above:

{% code %}
{% tab language="markup" title="Custom HEAD Tag" %}
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
{% /tab %}
{% /code %}