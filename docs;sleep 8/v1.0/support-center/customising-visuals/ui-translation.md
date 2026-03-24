---
type: page
title: UI Translation
listed: true
slug: ui-translation
description: 
index_title: UI Translation
hidden: 
keywords: 
tags: customisation
---

If you wish to change %product% UI  text that shows to your readers, which defaults to English, then you can modify it through two ways:

- Changing the Language from Documentation {% icon classes="fas fa-book inv-icon" /%} settings.
- Modifying the [javascript](/support-center/custom-javascript).

## Which Text Can be Changed?

{% image url="https://image-archive.developerhub.io/image/upload/-1/njdbubhyvukyseiqn5dd/1587679852.jpg" mode="responsive" height="724" width="1185" %}
{% /image %}

All text on the UI that we provide that shows to your reader can be translated. This includes text in landing page, search, table of contents as well as the version and section pickers.

The text that is available to be translated is detailed as such:

{% code %}
{% tab language="javascript" %}
{
  navbar: {
    home: 'Home',
  },
  tableOfContents: {
    title: 'On This Page'
  },
  search: {
    title: 'Search',
    singularResult: 'Showing ? search result',
    results: 'Showing ? search results',
    all: 'All',
    startTyping: 'Start typing to search...',
    searchTags: 'Search Tags',
    ai: {
      title: 'Search or ask a question',
      pressEnterToAsk: 'Press enter to ask',
      aiEnabled: 'AI enabled',
      askingAi: 'Asking AI',
      disclaimer: 'AI answers may be incorrect, incomplete or misleading. Refer to the sources.',
      answer: 'Answer'
    }
  },
  landingPage: {
    showAll: 'Show All',
    view: 'View',
  },
  documentations: 'Documentation',
  references: 'References',
  versions: 'Versions',
  page: {
    nextToRead: 'Next to read',
    relatedPages: 'Related pages',
    update: {
      lastUpdated: 'Last updated',
      by: 'by',
      on: 'on'
    },
    feedback: {
      prompt: 'Was this page helpful?',
      placeholder: 'Do you want to tell us more?',
      send: 'Send',
      skip: 'Skip',
      thankYou: 'Thank You!',
      yes: 'Yes',
      no: 'No'
    }
  },
  warnings: {
    oldVersion: 'You are viewing an older version. Click here to view the latest'
  },
  consent: {
    accept: 'Accept',
    text: 'We serve cookies on this site to analyse traffic and optimise your experience. By using the website you agree to the +Privacy Policy+.'
  },
  '404': {
    largeText: '404',
    smallText: 'It seems you are lost',
    button: 'Go back'
  }
}
{% /tab %}
{% /code %}

## Translate UI Text

To specify in which language should the UI text show in:

- From the sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Next to Language, select the language to translate the UI text to.

Each documentation can have its own translation.

At the moment, we have support for English, French, Deutsch and Spanish. If there is a language which you need for your documentation which we do not provide yet, then please [contact us](/support-center/contact-us).

## How to Customise UI Text

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

By using [custom javascript](/support-center/custom-javascript), you can modify any or all of the default translations. For example, you can add a script to your HEAD tags to override table of contents and search results as such:

{% code %}
{% tab language="html" title="Javascript" %}
<script>
  window.translations.apply({
  	tableOfContents: {
      title: "Tabla de contenido"
    },
    search: {
      results: "Mostrando ? resultados de búsqueda",
      singularResult: "Mostrando 1 resultado de búsqueda"
    }
  });
</script>
{% /tab %}
{% /code %}

{% callout type="info" title="Info" %}
Some translations contain variables such as `search.results` which will be replaced by the number of search results. The question mark indicates where the number will be replaced and must be kept in the translation.

Other translations such as `consent.text` have plus signs where a URL should be added.
{% /callout %}

### Change Translation According to Content

To change the UI text according to which version or which documentation is selected, then you can do that with [custom javascript](/support-center/custom-javascript). Example code that you can use:

{% code %}
{% tab language="html" title="Javascript" %}
<script>
	document.addEventListener('onsectionchange', function (event) {
        if (event.detail.type === 'documentation') {
            if (event.detail.slug === 'EN') {
				window.translations.tableOfContents.title = 'On This Page';
            } else if (event.detail.slug === 'DE') {
				window.translations.tableOfContents.title = 'Inhaltsverzeichnis';
            }
        }
    });
</script>
{% /tab %}
{% /code %}