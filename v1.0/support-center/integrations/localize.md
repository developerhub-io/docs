---
type: page
title: Localize
listed: true
description: 
index_title: Localize
hidden: false
keywords: 
tags: 
---

Localize easily translates websites and applications to new languages and streamlines your translation workflow.

To use Localize with %product%, you need to set up a script using [Custom HEAD Tags](../custom-javascript.md) as follows:

{% code %}
```html
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
```
{% /code %}

The two options `rememberLanguage` and `saveNewPhrasesFromSource` are recommended by Localize.

{% callout title="Info" %}
We handle variables in your docs as indicated by Localize.
{% /callout %}
