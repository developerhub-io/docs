---
type: page
title: Using Custom Domain
listed: true
slug: using-custom-domain
description: 
index_title: Using Custom Domain
hidden: 
keywords: 
tags: 
---

## What is a custom domain?

For example, if your website is hosted at hooli.com, then you can have your documentation hosted at `box.hooli.com`.

Your documentation reader will never have to leave your website and you still get the amazing experience of DeveloperHub.io documentation.

## How does it work?

Custom domain is available for supercharged plans. To set it up:

- Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Choose a custom subdomain such as `box.hooli.com` that exists under your own existing domain where you would like to have your documentation published on.
- Save the change.
- Configure your DNS records as in [Configure DNS](/support-center/configure-dns) page.
- When your documentation is published, then you can view it at either your custom domain or DeveloperHub.io subdomain.

## HTTPS Support

HTTPS is supported for all paid plans. If you are visiting your developer hub for the first time after setting up the custom domain, then it might take a few seconds for the SSL certificate to be created. After that, the website will load at normal speed.

If you are using CloudFlare, or any other hosting service which provides HTTPS for your custom domain out-of-the-box, then you may uncheck "Generate SSL Certificate" under Site Hosting.

## Site Verification

If you would like to enable Google Search Console, or any other Google product to your custom domain, you might need to verify the site ownership.

To enable the ownership, select the alternative methods option when prompted on Google's tools and choose using DNS verification.

If you are unable to use DNS verification, then you can then verify your ownership by adding a META tag by using [Custom HEAD Tags](/support-center/custom-javascript). However, you would either need to wait up to 7 days for the META tag to show for Google Site Verification bot, or you can [contact us](/support-center/contact-us) to speed up the process.