---
type: page
title: API Key
listed: true
slug: api-key
description: 
index_title: API Key
hidden: 
keywords: 
tags: 
---

%product% can integrate with your CI/CD pipelines to update pages and keep your references up to date.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1554055997/11500/pvyadjgik57ixpqzx9yi.png" mode="responsive" height="617" width="868" %}
{% /image %}

## Integrating with CI/CD

On running your CI/CD pipelines, you can upload a reference to %product% after generating it from your own tools. This works by:

- Generating your reference.
- Sending a request to %product% to update the reference.

If a reference with the same title already exists, then that reference will be updated. Otherwise, a new reference is created.

## How to Upload References Programmatically

To upload references programmatically:

### Create an API Key

To create an API Key for a project:

- In the sidebar, select API Key {% icon classes="fas fa-key inv-icon" /%}
- If you already have a key, then you can click on Copy to copy it.
- If not, then you can generate a new API Key.

Each API Key can have different permissions. Consult the [auto$](/v1.0/api/ref) to know which permissions you need.

### Upload Reference through API

To upload the reference through the API, check [Add or Update an API Reference](/v1.0/api/ref#add-reference) in our API Reference.

An example request would be:

{% code %}
{% tab language="bash" %}
curl --request POST \
    --url https://api.developerhub.io/api/v1/version/50/reference \
    --header "X-Api-Key: 689bbce8acc68b7a4346acca6a028e6f8126eb792b19a334f8e3f2a12ca8f561"
    --form "file=@/Users/DH/swagger.yaml"
{% /tab %}
{% /code %}