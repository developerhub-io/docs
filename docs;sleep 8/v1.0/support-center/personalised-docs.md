---
type: page
title: Personalised Docs
listed: true
slug: personalised-docs
description: 
index_title: Personalised Docs
hidden: 
keywords: 
tags: 
---

You can personalise the docs for your readers, so they no longer have to keep on jumping between different sources to find the information they need.

Things you might show in your docs that can be personalised:

- User ID,
- User Name,
- API Keys,
- API version they're currently using,
- Plan they are on,
- Their permissions...

## How to Personalise Docs

You can use [variables](/support-center/variables) to personalise the docs for your readers. For example, if you opened this documentation through our Help & Support then you would find your name %user.name% on the first page and also here.

Variables can be injected into the docs in two ways:

- By sending your readers to a docs URL having certain query parameters.
- By writing a [cookie](/support-center/personalised-docs#personalising-through-cookie).
- By using a [custom login](/support-center/custom-login) flow.

When the variables are injected, then the docs will show the information that is relevant to the reader.

## Personalising through URL

Variables can be injected into a page through the URL. You can provide the variables in two ways:

- Clear text: Add it in a URL query `vars`. For example `?vars={"user":{"name": "John"}}`
- Base64: Add it in a URL query `hvars`. For example `?hvars=eyJ1c2VyIjp7Im5hbWUiOiJKb2huIn19`

As an example, if you load this documentation from this link:

[https://docs.developerhub.io/?vars={"user":{"name": "John"}}](https://docs.developerhub.io/?vars=%7B%22user%22:%7B%22name%22:%22John%22%7D%7D)

{% callout type="info" title="Info" %}
The injected variables by URL would be stored for the user's session. It will persist until the browser is closed.
{% /callout %}

Then you will find yourself welcomed as a person named John.

## Personalising through Cookie

You can personalise (inject variables) by setting a cookie that your docs site can read. Using a cookie for personalisation is preferable to using URL personalisation as the variables would not get visible in the URL box.

The cookie is expected to be written outside of the docs site. For example, if you own `pied-piper.com` and your docs site is on `pied-piper.com/docs`, then you would write the cookie in `pied-piper.com` that is also readable on `pied-piper.com/docs`.

Cookies can only be readable on the same root domain regardless of the subdomain. For example, you can write cookie on: `pied-piper.com` and set it readable on `docs.pied-piper.com` as well as `pied-piper.com/docs`. However, if your docs site is on a different root domain such as `pied-docs.com` then you need to personalise through [URL or custom login](/support-center/personalised-docs#how-to-personalise-docs).

To inject variables using a cookie, provide the following in the cookie: 

{% code %}
{% tab language="none" %}
Name: vars
Value: eyJ1c2VyIjp7Im5hbWUiOiJKb2huIn19 # Base64 of the variables JSON
Domain: .docs.pied-piper.com # Custom domain of your docs
Path: / # Basepath of your docs, if you have multiple projects on same custom domain
Expires: Thu, 18 Dec 2022 12:00:00 UTC # As needed
HttpOnly: false
Secure: true
SameSite: Lax
{% /tab %}
{% /code %}

For example, to write such a cookie using javascript:

{% code %}
{% tab language="javascript" %}
let vars = {"user": {"name": "John"}};

document.cookie = "vars=" + btoa(JSON.stringify(vars)) + "; expires=Thu, 18 Dec 2022 12:00:00 UTC; path=/; domain=docs.pied-piper.com; SameSite=lax; Secure";
{% /tab %}
{% /code %}

## Standard for User Details

For personalising docs, we propose this standard for any features that we have or may build in the future. We recommend that you use the following JSON structure:

{% code %}
{% tab language="javascript" %}
{
  "user": {
    "id": 8
    "email": "email@address.com",
    "name": "User Name"
	}
}
{% /tab %}
{% /code %}