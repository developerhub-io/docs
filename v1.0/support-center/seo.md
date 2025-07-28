---
type: page
title: SEO
listed: true
slug: seo
description: 
index_title: SEO
hidden: 
keywords: 
tags: 
---

Your readers do not always start searching in your documentation and might look first through a search engine. If you are publishing your documentation with us on %product% subdomain or your own custom domain then you already are visible to search engines and all your content is indexed.

## Optimised for SEO

All our documentation portals are optimised for SEO. The pages are clearly structured and have canonical URLs which prevent content duplication. 

Each documentation, API reference and page can have its META description modified. You can even generate it using [auto$](/support-center/ai-summarisation).

We also show the best image and description for the content when pasting a documentation link on social media, slack, etc... You may also modify the description from **Page Info** (right sidebar).

{% callout type="info" title="Info" %}
We cache new SEO results every 7 days.
{% /callout %}

Our pages rank at 100% using Google's Lighthouse SEO test:

{% image url="https://uploads.developerhub.io/prod/02/tkxojqodsrgjtvcg92sum06d8yffmxpq0n02kbwiekx8chtdwa9qv8rslva99krk.png" caption="Google's Lighthouse SEO test on our pages" mode="600" height="1456" width="600" %}
{% /image %}

Furthermore, links are unfurled in external applications like Slack.

{% image url="https://uploads.developerhub.io/prod/02/rlu0qs6ug3n30m3l9m7b7bak9vrpm8ml7o3ng3vehgtgseoxr1p0ryui4p0yywbw.png" mode="responsive" height="461" width="702" %}
{% /image %}

## Sitemap

For SEO purposes, there is a sitemap that is available under `/sitemap.xml` of your subdomain and custom domain. If you are [hosting under an existing website](/support-center/hosting#hosting-under-an-existing-website), you should find it under `/sitemap.xml` of the subdomain, such as `<subdomain>.developerhub.io/sitemap.xml`, or under the basepath such as `docs.pied-piper.com/kb/sitemap.xml`.

You may also find the `robots.txt` file that we serve under `/robots.txt`. Furthermore, text sitemaps `sitemap.txt` are available.

{% callout type="info" title="Info" %}
Sitemaps are generated every 6 hours.
{% /callout %}

## When Using Custom Domain

If you are using your custom domain, you should create a property on the search engine's Search Console, such as [Google's Search Console](https://www.google.com/webmasters/tools/home). This will help you have control over the content published and get information about the search your readers are reaching you through.

## More Custom Options

By default, we indicate that the [short URL](/support-center/previewing-documentation#url-strategy) of the page without the version slug is the canonical URL. If you wish to change this to include the version slug, then you may do from Project Settings &gt; Under Hosting &gt; check "Canonicalize Short URL Form".

Also, if you wish to disable indexing for the non-default version, then you may do so from Project Settings &gt; Under Hosting &gt; check "Only Index Default Version".

Furthermore, if you wish to modify globally the titles of pages, then you may do so using [auto$](/support-center/advanced-settings) under `seo.titleFormats`.

To add META tags to provide more custom SEO options, descriptions, images and so on, check [auto$](/support-center/custom-javascript).

## Troubleshooting

### SEO software suite shows that all pages are empty

%product% renders the pages differently to actual readers vs. bots. These bots includes indexing spiders, site verification bots, SEO software spiders, AI agents, etc...

To view how a bot sees a page add `?_escaped_fragment_=` to the end of a URL. For example, if your page had the link `https://docs.developerhub.io/support-center/getting-started`, then the bot sees the page as `https://docs.developerhub.io/support-center/getting-started?_escaped_fragment_=`.

This is because our pages are dynamic and they get created as the reader views them, however spiders do not wait for the page to get created, so we serve them a static version of the page that has already loaded. This has no effect on SEO.

We have a long list of supported bots including all the major search engines, and SEO softwares such as SemRush, Ahrefs, Moz. If you are using a SEO software that seems to be unsupported by us, then either configure your SEO software to use a known spider user agent such as "googlebot", or [contact us](/support-center/contact-us) to add support for the SEO software.

### When I inspect the page source, the page is empty

Please see the [troubleshooting tip](/support-center/seo#seo-software-suite-shows-that-all-pages-are-empty) above. To view the source of the page, either open your browser's DevTools and view the source under Elements tab, or add `?_escaped_fragment_=` to the end of the URL and then view source normally.

### Search Engine report showing 404

If you are using any middleware (like Cloudflare) to serve your docs, then they might be affecting the ability for our caching servers to serve the pages to search engines. Disable the middleware for the docs site if possible.

### Getting a 403 or bad result

If you are using a firewall, your firewall might be blocking the requests from our SEO renderer. Please whitelist the user agent `DeveloperHub.io SSR`.

### Search Engine showing "Unable to Load Project"

Such issue happens when the docs are being cached by a middleware. Our docs are served differently according to the user agent header, which tells us if the user is a reader or a bot. To resolve the issue, either configure the cache to serve different version of the pages according to the user agent header, or disable the cache completely for the docs.

---

## Do Not Want To Be Visible?

If you do not want to be visible on search engines, you can uncheck "Enable Search Engines Indexing" in Project Settings.