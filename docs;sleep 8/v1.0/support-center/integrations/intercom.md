---
type: page
title: Intercom
listed: true
slug: intercom
description: 
index_title: Intercom
hidden: 
keywords: 
tags: 
---

Supercharged plan users can integrate %product% with Intercom to communicate with their users and to add a docs search widget in their messenger home.

{% image url="https://image-archive.developerhub.io/image/upload/5969/zqyhywd6ogykwn2xrrau/1539432578.png" mode="300" height="1330" width="300" %}
{% /image %}

## Setting up Intercom

- Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar to access Intercom settings under Integrations for Customers.
- Click Connect. You'll be taken through a flow to install %product% app on Intercom.

{% callout type="success" title="All set up!" %}
Intercom widget will now show on your published documentation.
{% /callout %}

{% image url="https://image-archive.developerhub.io/image/upload/5969/duevquzhwvpwpamdzhfm/1539432510.png" mode="600" height="1252" width="600" %}
{% /image %}

## Adding Search Widget

{% callout type="warning" title="Installed Intercom before 12 Aug 2023?" %}
If you had installed Intercom on %product% before 12 Aug 2023, you need to [contact us](/support-center/contact-us) to add the search widget.
{% /callout %}

{% callout type="info" title="Only in Default Layout" %}
Intercom can only show widgets when using the default layout messenger, not the compact layout.
{% /callout %}

To add a %product% search widget to your messenger home, ensure that you first have [set up Intercom](/support-center/intercom#setting-up-intercom), then:

- From Intercom's platform, click on Messenger & Omnichannel in the sidebar.
- Under Messenger, click on Manage Settings.
- Under Customise Home with apps, click on Add an app.
- Choose %product%.
- Change the card title if needed.

{% image url="https://uploads.developerhub.io/prod/02/ww5likoo946tze098bo5ofusyp5wpvsd6uclposbspv3abs0gx9dy4mrp1rc8gip.png" mode="300" height="1700" width="300" %}
{% /image %}

The search widget would use [auto$](/support-center/ai-search) if it is enabled.

## Changing Intercom Region or Settings

If Intercom widget is not showing after installing , check the DevTools console and network requests for error messages. Common issues include:

- `Your workspace is hosted in Europe but you connected to United States` which shows when the widget is trying to connect to the wrong data region.
- `This domain has not been trusted for the Intercom app defined in the JavaScript snippet.` which shows when you have not trusted your docs site in Intercom settings.

To apply your own `intercomSettings` for the widget, including if you wish to change the data region, then you can do so using [auto$](/support-center/custom-javascript). Add a script tag that assigns the `intercomSettings` needed, such as:

{% code %}
{% tab language="json" %}
<script>
  window.intercomSettings = {
    api_base: "https://api-iam.eu.intercom.io"
  };
</script>
{% /tab %}
{% /code %}