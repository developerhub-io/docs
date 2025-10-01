---
type: page
title: Search
listed: true
slug: using-search
description: 
index_title: Search
hidden: 
keywords: 
tags: 
---

%product% provides two search experiences:

- [Standard Search](/support-center/using-search#standard-search): Lightning-fast search service available for all paid plans. The search looks through each section of the documentation and links to it directly if a hit has been found. Typos are forgiven as well.
- [auto$](/support-center/ai-search): Search powered by GPT models that provide answers to questions with sources in natural language form.

The search bar exists at the top of the pages to attract attention and give the readers the best experience possible.

{% image url="https://image-archive.developerhub.io/image/upload/1011/sbj62viuedt8qlcrhxqf/1544135843.png" mode="responsive" height="335" width="734" %}
{% /image %}

### Look and Feel

The search bar shadow and the highlighting of the results uses the same branding colour that you have assigned as in [Customising Visuals](/support-center/customising-visuals#changing-colour).

{% callout type="info" title="Only in live mode" %}
Search is only available in live mode. The bar does show in editor mode, but it is just a demonstration. If you want to search for a page while in edit mode, then use the [Quick Switcher](/support-center/quick-switcher).
{% /callout %}

## Next UI Search

[Next UI](/support-center/customising-visuals#next-ui) provides a more powerful search experience for the readers. The search pops out for a larger search area, and provides controls for the reader to select the search scope.

{% image url="https://uploads.developerhub.io/prod/02/x4214x1qe2ok4wd8jfrzt0w8lckysq2mard4qdwz08qgy3z8v1w2ulap1x637kmg.png" mode="responsive" height="1376" width="1954" %}
{% /image %}

## Standard Search

Our standard search is lightning-fast search experience which provides readers with content relating to the terms queried.

### Search Speed

Our lightning-fast search has an average latency of less than 10 milliseconds.

### Search Update Frequency

We update the search index every 15 minutes. That means if you add or remove content, it will take up to 15 minutes for the content to show up in search.

## Page Keywords

You can add keywords to your page to enable your readers to find the page using those keywords. When using keywords, it is only useful when the word does not exist in the page itself. Thus, example of page keywords would be:

- Synonyms of words in the page.
- Words related to the page contents.
- Expansion of acronyms.

Page keywords can be added from the Page Info {% icon classes="fas fa-file-alt" /%} toolbar on the right side of the page.

## Change Search Scope

To change the search scope to only look into the active documentation or API reference, have a look at `search.scope` in our [auto$](/support-center/advanced-settings). 

## Searching using URL

If you wish to setup a search engine from your documentation, or you want to present your readers with a ready URL that searches the content for them, then you can do so by adding a `s` search query to any URL in your docs site. For example, by using this URL form: `https://<your-project-domain>/?s=%s` you'll be able to run search on a term (replace `%s`) directly as soon as the page loads. 

## Advanced Search Operators

Searching has the support for two advanced operators:

- Double quotations: Enclose terms in double quotations to only match exact matches. For example: `"search engine"` would only match when the words search engine exists and in this order. 
- Minus: Prohibit records with records prefixed by a minus sign. For example: `search -engine` would only match records having search, but not engine.

## Best Practices For Searchable Content

It is vital for the search to be able to pinpoint what the reader needs. Hence, it is important to arrange the content of your documentation as such:

- We split search results by using heading 2 only. Keep your heading 2 sections neither too short, nor too long. Any heading 2 content that is longer than 10 thousand characters (~2000 words, ~100 sentences) will be cut-off.
- Use as many varying words as possible, to ensure that whichever synonyms your readers might use are included in the text.

## Search using API

If you wish to provide documentation search capabilities outside of DeveloperHub, you can use our [Search](/v1.0/api/ref#search) to make queries and direct your users to the relevant documentation. An example search request would look like:

{% code %}
{% tab language="bash" %}
curl --request GET \
 --header "X-Api-Key: 689bbce8acc68b7a4346acca6a028e6f8126eb792b19a334f8e3f2a12ca8f561"
 --url https://api.developerhub.io/api/v1/search?query=best%20practices&version_slug=v1.0
{% /tab %}
{% /code %}

## Multi-Project Search

See [Enterprise Search](/support-center/enterprise-search) for more information about multi-project search.

## Javascript Hook for Search

If you wish to send search analytics to third party services, you can use the `onsearch` javascript event to handle all search operations. See [On Search event](/support-center/developer-tools#on-search).