---
type: page
title: FAQ
listed: true
slug: api-reference-faq
description: 
index_title: FAQ
hidden: 
keywords: 
tags: 
---

### Why is request/response body empty even though there is a schema object?

Check that your [schema object](https://swagger.io/specification/#schema-object) defines a type. If it doesn't, then we'll show the text `<type>` in the table. `properties` by itself is not enough to denote that the schema is an object.

For example:

{% code %}
{% tab language="yaml" title="Bad ❌" %}
content:
	application/json:
    schema:
      properties:
        id:
          type: number
        name:
         type: string
{% /tab %}
{% tab language="yaml" title="Good ✅" %}
content:
	application/json:
    schema:
      type: object <-- added
      properties:
        id:
          type: number
        name:
         type: string
{% /tab %}
{% /code %}

### How do I reorder Operations?

Operations (for example `GET /version` , `POST /reference`) are ordered according to how they are ordered in the OpenAPI definition itself. We use `tags` to group the operations, but we do not modify the order. For example:

{% code %}
{% tab language="yaml" %}
# If the operations and tags are specified as such in the API definition:

paths:
	'/cat':
  	post:
    	tags:
      	- Cats
      ...
    get: 
    	tags:
      	- Cats
      ...
  '/dog':
  	get: 
    	tags:
      	- Dogs
      ...
    post: 
    	tags:
      	- Dogs
      ...
tags:
	- name: 'Dogs'
  - name: 'Cats'
  
# The operations and tags would be ordered as such in the API reference:

# Dogs
#   GET  /dog
#   POST /dog
# Cats
#   POST /cat
#   GET  /cat
{% /tab %}
{% /code %}

Feel free to reorder the operations in your OpenAPI definition as needed to create the right journey for your readers.

To reorder, open the reference in our [API Editor](/support-center/edit-references) and edit the order of paths, operations, or tags directly in **Source** view — the reference re-renders in that order on save.