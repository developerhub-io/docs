---
type: page
title: Single Sign-On (SSO)
listed: true
slug: single-sign-on--sso-
description: 
index_title: Single Sign-On (SSO)
hidden: 
keywords: 
tags: 
---

{% callout type="warning" title="Editor SSO vs Reader SSO" %}
This page is about editors using SSO to sign in to %product%. If you're looking for readers using SSO to sign into your private docs, see [auto$](/support-center/reader-single-sign-on).
{% /callout %}

With SSO, you can manage your team access to %product% projects without having to add them one by one.

%product% easily integrates with your existing Identity Provider (IdP) so you can provide your employees with single sign-on to %product% using the same credentials and login experience as your other service providers.

By using SSO, you employees can access %product% directly from the shared dashboard your IdP provides, or through our login page. This brings you far more control over access and security.

%product% supports SAML 2.0, which works with but not limited to:

- Google
- Okta
- OneLogin
- Azure
- Active Directory (ADFS)

## Process for Setting Up SSO

The process for setting up SSO is as follows:

- [Contact us](/support-center/contact-us) to let us know that you require SSO, providing us with which IdP you are integrating with.
- We will provide you with an `sso_id` which you can use to get the ACS URL. The Entity ID and logo are as follows:
    - ACS URL: `https://auth.developerhub.io/login/callback/<sso_id>`
    - Entity ID: `https://auth.developerhub.io/sp`
    - [Logo link](https://res.cloudinary.com/developerhub/image/upload/v1561908888/1/gmoiyrndwsboeffgiz1x.svg).

- We will then require from you 
    - IdP SSO URL.
    - IdP Issuer.
    - Are responses signed?
    - X.509 certificate.

- Inform us of the [SSO configuration](/support-center/single-sign-on--sso-#configuration) you require.

{% callout type="info" title="Multiple SSO integrations" %}
If you have multiple SSO integrations with %product%, we can provide you with an alternative `entity ID` to be able to have multiple integrations on the same IdP. Please [contact us](/support-center/contact-us) for the alternative `entity ID`.
{% /callout %}

## Attributes

To save on time for your employees to enter their name on %product%, you can set **optional** attributes in your IdP setup as such:

- `firstname` and `lastname` for First Name and Last Name of a user profile.
- `name` if your user profiles have full names.
- `role` to one of `ADMIN`, `PUBLISHER`, `WRITER`, `REVIEWER`.

### Google SSO

While configuring SSO, use `EMAIL` Name ID format with `Basic Information > Primary email`.

The attributes for Google SSO must look as follows:

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1621016202/v2_1/uj1k8qntxsf2bq5ahttj.jpg" mode="responsive" height="528" width="1175" %}
{% /image %}

### Okta SSO

While configuring SSO, use Name ID format `EmailAddress` and Application username to be `Email`.

The attributes for Okta SSO must look as follows:

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1621016253/v2_1/ygliplh25qaaysj5jzm2.jpg" mode="responsive" height="300" width="702" %}
{% /image %}

## Configuration

%product% provides configuration settings for SSO connections. They are:

- SSO login enforced: Specifies if editors can only log in using SSO. By default this is disabled until SSO connection is tested.
- Default role: The default [role](/support-center/collaboration#user-roles) for users that get created by signing into SSO.
- Add users to all projects by default: Specifies whether when a user logs in, they would have access to all the projects in the organisation, or if they would require an invitation for each project.
- Email domain: (Optional) The organisation email domain (e.g. `tesla.com`). Used when new users are logging in using SSO.

SSO settings can be viewed by organisation owners from the sidebar &gt; Organisation {% icon classes="fas fa-building inv-icon" /%}. SSO settings can be changed by [contacting us](/support-center/contact-us).

## Creating Users

To create/invite users into your project, you can:

- Initiate a session from your IdP.
- Provide them with a link which you can copy from Team {% icon classes="fas fa-user-cog inv-icon" /%} &gt; Copy SSO Login URL {% icon classes="far fa-copy" /%}
- Invite them by e-mail address from Team {% icon classes="fas fa-user-cog inv-icon" /%} &gt; Invite teammate to collaborate {% icon classes="fas fa-plus" /%}. They will be sent an e-mail containing the SSO Login URL.
- Ask them to log in directly from [our login screen](https://app.developerhub.io/login) if "Email domain" is configured for the SSO connection.

## Logging in Users

To login existing users, they can:

- Initiate a session from your IdP.
- Provide them with a link which you can copy from Team {% icon classes="fas fa-user-cog inv-icon" /%} &gt; Copy SSO Login URL {% icon classes="far fa-copy" /%}.
- Login directly from [our login screen](https://app.developerhub.io/login) by using **Log in Using SSO**.

## Deprovisioning Users

When deprovisioning a user, the following will happen:

- All their projects will be removed, regardless if they are in the organisation or not.
- All their access to the organisation's projects will be revoked.
- Their user account will be deleted. If they needed to be re-activated again, the user will be a new user.

To deprovision a user:

- From the sidebar, click on Team {% icon classes="fas fa-user-cog inv-icon" /%}.
- Click on the badge next to the user, and click **Deprovision from Organisation**.
- Confirm your choice.

{% callout type="warning" title="Action cannot be undone" %}
Once a user is deprovisioned, their own projects and user account are removed from our system - there's no turning back.
{% /callout %}

## Debugging SSO Issues

If on SSO login you get a message, which depends on your IdP, indicating that the user is not allowed in this application, then you should ensure that the user is added to the correct group in your IdP application settings.