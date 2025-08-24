---
type: page
title: Edit References
listed: true
slug: edit-references
description: 
index_title: Edit References
hidden: 
keywords: 
tags: 
---

With %product% you can edit your OpenAPI 2/3 definitions using our visual API editor that is powered by Apicurio.

{% image url="https://uploads.developerhub.io/prod/02/87uyuvaekjddt88824m037v0lf1cn5gwx4lawhpn3yc6d25opz8j85654qadhdks.png" mode="responsive" height="1827" width="2920" %}
{% /image %}

## OpenAPI Editor Features

The OpenAPI Editor is a fully-featured visual web-based editor that supports OpenAPI versions 2.0, 3.0.0, 3.0.1, 3.0.2 and 3.0.3. (OpenAPI v3.1.0+ support is upcoming). It helps you build the schema of your OpenAPI reference without needing to know the ins and outs of the specification.

## Editing an API Definition

To edit an existing API definition:

- From the sidebar, choose Reference {% icon classes="fas fa-vector-square" /%}.
- Choose the API Reference to be edited from the list.
- Once the API Reference has loaded, click on Edit in the bottom right side of the screen. The API Editor will load in a new tab.
- Make the changes. Click Save Draft when done.

Once you are ready to publish the API Reference, a publisher may click Publish button on the API Reference.

## Create a new API Definition

To create a new API definition using our OpenAPI editor:

- From the sidebar, choose Reference {% icon classes="fas fa-vector-square" /%}.
- Choose "Create new OpenAPI 3 reference". The API editor will launch in a new tab.

## Generators

Do you prefer to generate the OpenAPI file directly from code so it is always up to date with your codebase? Here are a few generators from source-code:

- Javascript: [swagger-jsdoc](https://www.npmjs.com/package/swagger-jsdoc)
- Express: [swagger-express](https://www.npmjs.com/package/swagger-express)
- PHP: [swagger-php](https://github.com/zircote/swagger-php)
- Symfony: [NelmioApiDocBundle](https://github.com/nelmio/NelmioApiDocBundle)
- Django: [django-rest-swagger](https://github.com/marcgibbons/django-rest-swagger)
- Flask: [flask-restplus](https://github.com/noirbizarre/flask-restplus)
- Ruby On Rails: [openapi-rails](https://github.com/slate-studio/openapi-rails)
- Go: [go-swagger](https://goswagger.io/)
- Spring: [springfox](https://github.com/springfox/springfox)

You can use our [API to upload API references automatically](/support-center/api-key#how-to-upload-references-programmatically).