---
type: page
title: Server Headers
listed: true
slug: server-headers
description: 
index_title: Server Headers
hidden: 
keywords: 
tags: 
---

You may want to set up extra server headers for security purposes. The headers are returned when a client requests your docs site.

## How to set up Server Headers?

To set up server headers:

- From the sidebar, click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Hosting, click on Edit Headers {% icon classes="fas fa-server" /%}.
- Add the server headers as follows:
    - Each header must be on one line.
    - Each header must have the header name and value separated by `:`.
    - You cannot modify certain headers, such as `Cache-Control` or `Server`.
    - Any invalid header will be removed.

- Hit Save.

It may take up to 5 minutes for changes to take effect.

## Example Security Headers

These are some security headers that you may want to apply.

{% callout type="warning" title="Caution" %}
Make sure you fully understand what each header is. Using headers incorrectly could cause your entire custom domain to be **irreversibly broken**. We are not liable for any damages due to misconfiguration.
{% /callout %}

{% code %}
{% tab language="yaml" title="Headers" %}
Strict-Transport-Security: max-age=31536000
X-Frame-Options: DENY
Referrer-Policy: no-referrer
{% /tab %}
{% /code %}