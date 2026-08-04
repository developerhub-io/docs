---
type: page
title: Configure DNS
listed: true
description: 
index_title: Configure DNS
hidden: false
keywords: 
tags: 
---

## Why to configure DNS?

You only need to configure your DNS if you have a custom domain registered with %product%. DNS configuration is required for the custom domain to serve a %product% documentation.

## What happens when you configure Custom Domain?

After completing these steps, you should be able to access your %product% documentation through the custom domain your setup. For example, if the setup custom domain is `box.hooli.com` then your documentation will be accessible from there for your readers.

## How to configure DNS?

You need access to your DNS configuration. If you are not sure who might have access, then it is most likely it is your IT Admin. The only configuration needed is to setup a CNAME record that matches the host `you.developerhub.io` to the custom domain that you set up. To summarise, the DNS CNAME record should match:

{% table layout="auto" %}
{% row %}
{% cell header=true %}
Name
{% /cell %}
{% cell header=true %}
Type
{% /cell %}
{% cell header=true %}
Value
{% /cell %}
{% /row %}
{% row %}
{% cell %}
The custom domain you set e.g. `developers.xyz.com`
{% /cell %}
{% cell %}
`CNAME`
{% /cell %}
{% cell %}
`you.developerhub.io`
{% /cell %}
{% /row %}
{% /table %}

{% callout title="Info" %}
DNS configuration might take a few minutes up to a few hours, depending on your DNS provider, to be effective.
{% /callout %}

{% callout type="warning" title="Warning" %}
Ensure that your domain's CAA record does not deny `letsencrypt.org` to issue certificates.

You can check it using [NS Lookup](https://www.nslookup.io/domains/developerhub.io/dns-records/caa/). It should either note that your domain does not have a CAA record, or it must list `letsencrypt.org`. Otherwise, we are unable to issue an SSL certificate to enable HTTPS.
{% /callout %}

{% accordion-group %}
{% accordion title="Can I use a root domain?" %}
While it might be technically possible to use a root domain such as `hooli.com` to serve your documentation, it might bring technical debt for you later on. DNS CNAME records do not play well with other DNS records such as `MX` for mail. This is a limitation of the DNS systems, not a %product% limitation.
{% /accordion %}
{% /accordion-group %}

## Need help configuring your DNS?

Let us know if you need help setting up the DNS configuration by talking to us through the Let's Talk button below 👇.
