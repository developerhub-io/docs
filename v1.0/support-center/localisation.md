---
type: page
title: Localisation
listed: true
slug: localisation
description: 
index_title: Localisation
hidden: 
keywords: 
tags: 
---

%product% provides localisation for your documentation in two ways:

- Using an automated third party service, such as [Localize](localizejs.com).
- By using different documentation for different languages.

## Localise using Localize

Localize easily translates websites and applications to new languages and streamlines your translation workflow.

To use Localize with %product%, you need to set up a script using [Custom HEAD Tags](/support-center/custom-javascript) as follows:

{% code %}
{% tab language="html" %}
<script>
  (function(d, script) {
      script = d.createElement('script');
      script.type = 'text/javascript';
      script.async = true;
      script.onload = function(){
          !function(a){if(!a.Localize){a.Localize={};for(var e=["translate","untranslate","phrase","initialize","translatePage","setLanguage","getLanguage","detectLanguage","getAvailableLanguages","untranslatePage","bootstrap","prefetch","on","off","hideWidget","showWidget","getSourceLanguage"],t=0;t<e.length;t++)a.Localize[e[t]]=function(){}}}(window);

          Localize.initialize({
            key: 'YOUR_PROJECT_KEY',
            rememberLanguage: true,
            saveNewPhrasesFromSource: true
            // other options go here, separated by commas
          });
      };
      script.src = 'https://global.localizecdn.com/localize.js';
      d.getElementsByTagName('head')[0].appendChild(script);
  }(document));
</script>
{% /tab %}
{% /code %}

The two options `rememberLanguage` and `saveNewPhrasesFromSource` are recommended by Localize.

{% callout type="info" title="Info" %}
We handle variables in your docs as indicated by Localize.
{% /callout %}

## Localise using different documentation

To localise using different documentation, you would need to [create documentation](/support-center/managing-documentation#creating-documentations) for each language.

For example, in your v1.0 version, you can have the following documentation sections: `en`, `de`, and `es`. If you already had multiple documentation, for example for `Android SDK`, `iOS SDK` and so on, then you can expand your documentation to `Android SDK (EN)`, `Android SDK (DE)` and `Android SDK (ES)`, and so on.

We also provide the option for you to customise the UI text to better suit your needs. For detailed instructions, please refer to [UI translation](/support-center/ui-translation).

## Which localisation method should I choose?

It depends on the complexity of your docs and resources.

If your docs are of a manageable size, and you do have the resources to keep up with documentation changes in one language, and to replicate it to other languages, then you can use different documentation for each language.

If your docs are of a large size, and you would like the easiest most effective solution, then you would want to use Localize or another third party service. Using an automated third party service makes it easier for you to keep all parts of your documentation up-to-date with all the languages you wish to offer. Once content is added or modified, you will be prompted to approve the new translations. This ensure that your docs cannot go out-of-sync. Also, you would not need to modify your project structure.