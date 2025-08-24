---
type: page
title: Graphs/Charts
listed: true
slug: graphs-charts
description: 
index_title: Graphs/Charts
hidden: 
keywords: 
tags: 
---

The web is full of different graphing/charting open-source libraries. The good news is that if it has a javascript API, then you can use [Custom Javascript](/support-center/custom-javascript) with [Custom HTML](/support-center/custom-html) to render directly on the page. In this page, we'll look into how to add the integration for different libraries.

## Mermaid Charts

[MermaidJS](https://mermaid-js.github.io) lets you create diagrams and visualisations using text and code. To use it in %product%, set up a Custom HTML block with such contents:

{% code %}
{% tab language="markup" title="Custom HTML" %}
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<div class="mermaid">
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
</div>
<script>
   mermaid.init();
   window.postMessage('resize', '*'); // resizes the container to remove scroll
</script>
{% /tab %}
{% /code %}

Rendered as such:

{% html %}
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<div class="mermaid">
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
</div>
<script>
   mermaid.init();
   window.postMessage('resize', '*');
</script>
{% /html %}

## WebSequenceDiagrams

[WebSequenceDiagrams](https://www.websequencediagrams.com/) creates sequence diagrams. To use it in %product%, add a Custom HTML block with such contents:

{% code %}
{% tab language="markup" title="Custom HTML" %}
<div class=wsd wsd-style="modern-blue" ><pre>

Alice->Bob: Authentication Request
Bob-->Alice: Authentication Response

</pre></div><script type="text/javascript" src="https://www.websequencediagrams.com/service.js"></script>
{% /tab %}
{% /code %}

Rendered as such:

{% html %}
<div class=wsd wsd-style="modern-blue" ><pre>

Alice->Bob: Authentication Request
Bob-->Alice: Authentication Response

</pre></div><script type="text/javascript" src="https://www.websequencediagrams.com/service.js"></script>
{% /html %}

## PlantUML

[PlantUML](https://plantuml.com/) is a component that allows you to quickly write many kinds of diagrams. To use it in %product%, add a Custom HTML block with such contents:

{% code %}
{% tab language="html" title="Custom HTML" %}
<head>
  <script src="//cdn.rawgit.com/jmnote/plantuml-encoder/d133f316/dist/plantuml-encoder.min.js"></script>
</head>
<body>
  <uml>
@startuml
Bob -> Alice : hello
@enduml
  </uml>
  <script>
    var el = document.getElementsByTagName('uml')[0];
    var src = "//www.plantuml.com/plantuml/svg/" + window.plantumlEncoder.encode(el.textContent);
    var img = document.createElement('IMG');
    img.src = src;
    img.style.maxWidth = '100%';
    img.onclick = function() {window.postMessage({zoomImage: src}, '*')};
    el.replaceWith(img);
    window.postMessage('resize', '*');
  </script>
</body>
{% /tab %}
{% /code %}

Replacing the contents of UML element with the desired UML.

Rendered as such:

{% html %}
<head>
  <script src="//cdn.rawgit.com/jmnote/plantuml-encoder/d133f316/dist/plantuml-encoder.min.js"></script>
</head>
<body>
  <uml>
@startuml
Bob -> Alice : hello
@enduml
  </uml>
  <script>
    var el = document.getElementsByTagName('uml')[0];
    var src = "//www.plantuml.com/plantuml/svg/" + window.plantumlEncoder.encode(el.textContent);
    var img = document.createElement('IMG');
    img.src = src;
    img.style.maxWidth = '100%';
    el.replaceWith(img);
    window.postMessage('resize', '*');
  </script>
</body>
{% /html %}

## JSON Crack

[JSON Crack](https://jsoncrack.com/) is a JSON viewer tool to visualise, format and modify. To use it in %product%, add a Custom HTML block with the embed contents, styling the `iframe`:

{% code %}
{% tab language="html" %}
<iframe style="border: none; width: 100%; height: 300px;" 
        src="https://jsoncrack.com/widget?json=639b65c5a82efc29a24b2de2" />
{% /tab %}
{% /code %}

Rendered as such:

{% html %}
<iframe style="border: none; width: 100%; height: 300px;" 
        src="https://jsoncrack.com/widget?json=639b65c5a82efc29a24b2de2" />
{% /html %}