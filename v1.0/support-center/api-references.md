---
type: page
title: API References
listed: true
description: 
index_title: API References
hidden: false
keywords: 
tags: 
---

%product% generates beautiful and powerful API References from your API definitions. [Create](edit-references.md#create-a-new-api-definition), [upload](uploading-references.md), [merge](merge-api-definitions.md) or [edit](edit-references.md) your OpenAPI definitions directly on %product%.

See our [own API References](/v1.0/api/ref) here.

{% video provider="raw" videoId="https://uploads.developerhub.io/prod/02/alfw0asaqyh1rzb2dnud9xzobfsc2l255qvbqq2pd97nrgz3pkd22pe6thc23xwm.mp4?controls=0&autoplay=1&loop=1&muted=1&playsinline=1" /%}

## Features

Your beautiful API References consist of:

- A title heading with a summary.
- All available server URLs.
- Authentication methods.
- All the operations listed grouped by tags.
- All webhooks (OAS 3.1+).

Every operation shows the following:

- Summary and information.
- Headers.
- Request and response media types.
- Query parameters, path parameters, body data and form data.
- Response codes and response bodies.
- Property constraints.
- Auto-generated example request using [different libraries](api-references/code-generation.md).
- Auto-generated example responses.
- Callbacks.

{% image url="https://uploads.developerhub.io/prod/02/kaafjmio918q0icqrl992zgctenx5bei9s0m4hg4ar1tnn64l4fe200iwor313sn.png" width=1038 /%}

You can directly link to the API references from the documentation by following the steps in [page linking](writing-documentation/page-linking.md).

{% image url="https://uploads.developerhub.io/prod/02/s9c05oknkjn80rj50fxddju1d4nkjnviqerqy3gldz2mq6c2nogv7jges35f6svc.png" /%}

## Try It Out

{% image url="https://uploads.developerhub.io/prod/02/aja6dp81xp8atteilzyxqz0n1ceimluy4667m0y5g4u7r97ryj80f1y6s6bymmh2.png" /%}

Readers can [try out your API](try-it-out.md) right from the API Reference.

## API Reference Personalisation

You can personalise your API references, so your readers do not have to fetch the dynamic variables out from different places.  See [variables](variables.md) and [personalised docs](personalised-docs.md) for implementation.

## Supported Specifications

We support OpenAPI 3.2, 3.1, 3.0 and OpenAPI 2.0 (legacy Swagger).

## File Type

These types are supported:

- JSON files - .json
- YAML files - .yaml
