---
type: page
title: Hosting
listed: true
slug: hosting
description: Host your documentation easily with DeveloperHub. Choose between hosting on a subdomain, a custom domain, or under your existing website. Multiple projects? No problem! Learn more about hosting options and how to optimize performance.
index_title: Hosting
hidden: 
keywords: 
tags: 
---

%product% makes hosting a breeze for you. We offer multiple ways in which you can have your docs hosted:

- On a [subdomain](/support-center/project-settings#changing-subdomain) of %product%, such as `pied-piper.developerhub.io`.
- On an unused [custom domain](/support-center/using-custom-domain) that you own, such as `docs.pied-piper.com`.
- Under [your existing website](/support-center/hosting#hosting-under-an-existing-website), such as `pied-piper.com/docs`.

You can also host multiple projects on the same site.

{% callout type="warning" title="Changing hosting settings" %}
If you modify hosting settings after your docs have already been published, then make sure that you are able to redirect any external links to your new docs. Also, redirecting helps to keep your SEO ranking unaffected.
{% /callout %}

## Which Hosting Option is Better?

Your readers would like to get a familiar URL when they visit your docs, so we always encourage you to host the docs on a domain that you own, like `pied-piper.com`.

However, it isn't only readers that access your docs. In fact, all kinds of bots and crawlers access it as well to index it for search engines. Allowing the search engines to crawl is very important for your search ranking. For search engines, every host is a different entity, that is unrelated to the root domain. For example, `docs.pied-piper.com` has a completely different ranking than `pied-piper.com`.

If you are starting with a docs site for the first time at `docs.pied-piper.com`, then you're starting with a fresh slate. Your ranking still has to grow from the start. So we recommend that you use [Hosting under an Existing Website](/support-center/hosting#hosting-under-an-existing-website) hosting option so you can pick up the ranking from your root domain at `pied-piper.com` since that is probably where all the marketing has been done previously.

If you already had a docs site and you're moving to %product%, then you are picking up the ranking you already had.

In conclusion: Use [Hosting under an Existing Website](/support-center/hosting#hosting-under-an-existing-website) if possible, otherwise it's totally fine to host [auto$](/support-center/using-custom-domain).

## Hosting under %product% Subdomain

To set or change the subdomain:

1. Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Subdomain, click on Edit to enable edit mode.
3. Change the subdomain.
4. Click on Save. If the subdomain was already taken, then you will be notified.

## Hosting under your own Custom Domain

Follow the steps in [auto$](/support-center/using-custom-domain).

## Hosting under an Existing Website

{% callout type="info" title="Access to Server" %}
You must have access to your server configuration files to host under an existing website
{% /callout %}

If you already have a website, for example `pied-piper.com` and you would like to host your docs under `pied-piper.com/docs`, then you can do this by modifying the basepath and setting up a reverse proxy from your servers. A step-by-step guide is as follows:

- On %product%:
    1. Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
    2. Enter the basepath where your want your docs to live, such as `docs` or `hooli`. It could be a deeper subdirectory, such as `docs/project1`.
    3. Under Basepath, click on Edit to enable edit mode.
    4. Click on Save.
    5. Under Custom Domain, click on Edit to enable edit mode.
    6. Enter the host where the existing website lives, such as `pied-piper.com` or `support.pied-piper.com`.

- On your server:
    - Set up a reverse proxy to your %product% subdomain, such as with nginx. Here is an example configuration:

{% code %}
{% tab language="bash" title="docs.conf" %}
server {
  server_name <custom-domain>; # e.g. server_name support.pied-piper.com

  location /docs {
    proxy_pass https://<subdomain>.developerhub.io; # e.g. proxy_pass https://piper.developerhub.io
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
    proxy_set_header Host $host;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Uri $request_uri;
  }
}
{% /tab %}
{% /code %}

Make sure that you do not add trailing forward slashes for `location` URI and `proxy_pass` URI as indicated in the example. Adding them may break SEO or domain settings.

{% callout type="warning" title="Warning" %}
HTTPS must be used, so ensure that your existing website already has a valid certificate.
{% /callout %}

{% callout type="info" title="Info" %}
You do not need to modify [DNS records](/support-center/configure-dns) or to follow [auto$](/support-center/using-custom-domain) to host under an existing website.
{% /callout %}

You may also use the approach above to set up your own custom redirection rules if needed, leaving the base path empty.

### Setting up your application firewall when hosting under an existing website

When you are hosting under an existing website and you have an application firewall running, you must perform the following:

1. Whitelist `DeveloperHub.io SSR` user agent for all URLs in the docs site. This ensures that we can serve the pages to search indexing robots for SEO purposes. See [SEO troubleshooting](/support-center/seo#getting-a-403-or-bad-result).
2. Whitelist `DeveloperHub.io PDF Exporter` user agent for all URLs in the docs site. This ensures that PDF exports are enabled.

## Hosting Multiple Projects under One Site

To host multiple projects under one site, you can set multiple projects to be on a single subdomain or a single custom domain. You must be the owner of all these projects. If you are under an enterprise plan, then all of the projects must be in the same organisation.

For example, you may setup three projects to be as such:

- Project: Product Documentation
    - Custom domain: `docs.pied-piper.com`.
    - No base path.
    - Accessible at `https://docs.pied-piper.com/`.

- Project: Knowledge Base
    - Custom domain: `docs.pied-piper.com`.
    - Base path: `kb`.
    - Accessible at `https://docs.pied-piper.com/kb`.

- Project: Release Notes
    - Custom domain: `docs.pied-piper.com`.
    - Base path: `release-notes`.
    - Accessible at `https://docs.pied-piper.com/release-notes`.

When multiple projects are hosted under a subdomain or a domain, {% icon classes="fas fa-sitemap" /%} will show next to the setting input.

## Performance Troubleshooting

If your docs site is loading slow, then you might want to check any middleware (such as Cloudflare) that you are using to serve the domain. Also, if you are using reverse proxy then ensure that your servers are performant. Furthermore, if you are using any middleware, ensure that the middleware is passing the query string to our servers, otherwise some functionality might not work.

Our own docs load in under 200ms from Europe. Our largest docs load in under 1s from San Fransisco.