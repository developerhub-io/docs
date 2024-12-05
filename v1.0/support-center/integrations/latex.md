---
type: page
title: Latex
listed: true
slug: latex
description: 
index_title: Latex
hidden: 
keywords: 
tags: 
---

{% callout type="warning" title="Javascript backslash" %}
For all equations written in javascript, remember to escape the `\` with another `\`. `\` by itself is an escape delimiter.
{% /callout %}

## LaTeX.js

Project homepage: [https://latex.js.org/](https://latex.js.org/)

{% html %}
<!DOCTYPE html>
<html lang="en">
<head>
  <script src="https://cdn.jsdelivr.net/npm/latex.js/dist/latex.js"></script>
</head>

<body>
  <script>
    var text = 'The fraction is as such: $\\frac{\\sqrt{2}}{2}$'

    var generator = new latexjs.HtmlGenerator({ hyphenate: false })

    generator = latexjs.parse(text, { generator: generator })
    document.head.appendChild(generator.stylesAndScripts("https://cdn.jsdelivr.net/npm/latex.js@0.12.4/dist/"))
    document.body.appendChild(generator.domFragment())
  </script>
</body>

</html>
{% /html %}

Code:

{% code %}
{% tab language="html" %}
<!DOCTYPE html>
<html lang="en">
<head>
  <script src="https://cdn.jsdelivr.net/npm/latex.js/dist/latex.js"></script>
</head>
<body>
  <script>
    var text = 'The fraction is as such: $\\frac{\\sqrt{2}}{2}$'

    var generator = new latexjs.HtmlGenerator({ hyphenate: false })

    generator = latexjs.parse(text, { generator: generator })
    document.head.appendChild(
      generator.stylesAndScripts("https://cdn.jsdelivr.net/npm/latex.js@0.12.4/dist/"))
    document.body.appendChild(generator.domFragment())
  </script>
</body>
</html>
{% /tab %}
{% /code %}

## KaTex

Project homepage: [https://katex.org/](https://katex.org/)

{% html %}
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.css" integrity="sha384-Xi8rHCmBmhbuyyhbI88391ZKP2dmfnOl4rT9ZfRI7mLTdk1wblIUnrIq35nqwEvC" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.js" integrity="sha384-X/XCfMm41VSsqRNQgDerQczD69XqmjOOOwYQvr/uuC+j4OPoNhVgjdGFwhvN02Ja" crossorigin="anonymous"></script>
  </head>
  <body>
    <span id="container"></span>
    <script>
      katex.render("c = \\pm\\sqrt{a^2 + b^2}", document.getElementById("container"), {
        displayMode: true
      });
    </script>
  </body>
</html>
{% /html %}

Code:

{% code %}
{% tab language="html" %}
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.css" integrity="sha384-Xi8rHCmBmhbuyyhbI88391ZKP2dmfnOl4rT9ZfRI7mLTdk1wblIUnrIq35nqwEvC" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.js" integrity="sha384-X/XCfMm41VSsqRNQgDerQczD69XqmjOOOwYQvr/uuC+j4OPoNhVgjdGFwhvN02Ja" crossorigin="anonymous"></script>
  </head>
  <body>
    <span id="container"></span>
    <script>
      katex.render("c = \\pm\\sqrt{a^2 + b^2}", document.getElementById("container"), {
        displayMode: true
      });
    </script>
  </body>
</html>
{% /tab %}
{% /code %}