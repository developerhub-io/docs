---
type: page
title: POWr Integration
listed: false
slug: powr-integration
description: 
index_title: POWr Integration
hidden: 
keywords: 
tags: 
---

Custom HEAD tag:

{% code %}
{% tab language="html" %}
<script src="https://www.powr.io/powr.js?platform=<<platform>>"></script>
<script>
  window.powrform = null;
	document.addEventListener('onpagechange', function (event) {
    if (window.powrform) {
    return;
    }
    var master = document.querySelector('app-documentation-content>.master');
    var form = document.createElement('DIV');
    form.classList.add('powr-feedback-form');
    form.id = '<<id>>';
    master.insertAdjacentElement('afterend', form);
    window.powrform = form;
  });
</script>
{% /tab %}
{% /code %}