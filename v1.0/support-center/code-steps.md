---
type: page
title: Code Steps
listed: true
slug: code-steps
description: 
index_title: Code Steps
hidden: 
keywords: 
tags: 
---

{% code-steps title="Code Steps" description="There goes the description" %}
{% step title="Step one" description="This is a very detailed description of the first step" codeId="code-1" %}
{% /step %}
{% code id="code-1" language="javascript" title="math.class.ts" %}
function add(x, y) {
  return x + y;
}
{% /code %}
{% /code-steps %}