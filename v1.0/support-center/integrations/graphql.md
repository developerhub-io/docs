---
type: page
title: GraphQL
listed: true
slug: graphql
description: 
index_title: GraphQL
hidden: 
keywords: 
tags: 
---

To embed a GraphiQL playground in a page, get the embed code from [embed.graphql.com](embed.graphql.com) and paste it into a [auto$](/support-center/custom-html) block. For example:

{% code %}
{% tab language="html" title="Custom HTML" %}
<iframe title="GraphiQL" width="100%" height="500" src="https://embed.graphql.com/embed?endpointURL=%22https%3A%2F%2Fcountries.trevorblades.com%2F%22&query=%22query%20%7B%5Cn%20%20countries%20%7B%5Cn%20%20%20%20capital%5Cn%20%20%20%20currency%5Cn%20%20%7D%5Cn%7D%5Cn%22&variables=%22%22&response=%22Hit%20run!%5Cn%22&history=false&prettify=true&docs=true" />
{% /tab %}
{% /code %}

Would render:

{% html %}
<iframe title="GraphiQL" width="100%" height="500" 
        src="https://embed.graphql.com/embed?endpointURL=%22https%3A%2F%2Fcountries.trevorblades.com%2F%22&query=%22query%20%7B%5Cn%20%20countries%20%7B%5Cn%20%20%20%20capital%5Cn%20%20%20%20currency%5Cn%20%20%7D%5Cn%7D%5Cn%22&variables=%22%22&response=%22Hit%20run!%5Cn%22&history=false&prettify=true&docs=true" />
{% /html %}

You may even set this up in a [auto$](/support-center/custom-landing-page) for full width experience. See [auto$](/graphql-test) for an example.