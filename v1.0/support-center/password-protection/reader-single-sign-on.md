---
type: page
title: Reader Single-Sign On
listed: true
slug: reader-single-sign-on
description: 
index_title: Reader Single-Sign On
hidden: 
keywords: 
tags: 
---

With SSO, you can manage reader access to a %product% docs site using an identity provider.

%product% supports SAML 2.0, which works with but not limited to:

- Google
- Okta
- OneLogin
- Azure
- Active Directory (ADFS)

## Process for Setting Up SSO

The process for setting up SSO is as follows:

- [Contact us](/support-center/contact-us) to let us know that you require SSO, providing us with which IdP you are integrating with.
- We will provide you with an `sso_id` which you can use to get the ACS URL. The ACS URL and Entity ID are as follows:
    - ACS URL: `https://auth.developerhub.io/login/callback/<sso_id>`
    - Entity ID: `https://auth.developerhub.io/reader`

- We will then require from you the IdP SSO URL, the IdP Issuer and a X.509 certificate.

## Logging in Readers

To login readers, they can:

- Initiate a session from your IdP.
- Login directly through the docs site.