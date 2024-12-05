---
type: page
title: Email Invite (Magic Links)
listed: true
slug: email-invite
description: 
index_title: Email Invite (Magic Links)
hidden: 
keywords: 
tags: 
---

With Magic Links, your private project can only be accessed by those whom you invite.

{% image url="https://uploads.developerhub.io/prod/02/dbxagnkoxv0fytzpry413esklxm3mtb8pa43c9ykfp72q6djna5pcaqxh1k92exf.png" mode="responsive" height="603" width="949" %}
{% /image %}

## How do Magic Links work?

The process is as follows:

- You invite a reader by providing their e-mail address and when their access should expire (or never).
- We send them an e-mail containing a link that allows them access to the docs for the validity of their access. Once they use the link, it can no longer be used again.
- If they need another link, they can always go to the docs site and request a new magic link.

## How to Enable Email Invite?

1. From the sidebar, choose Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
2. Under General Settings, choose Make Private (or Manage Access).
3. Select Email Invite.
4. Hit Save.

## How to Invite Readers?

To invite readers:

1. First, ensure that the project is protected by Email Invite.
2. From the sidebar, choose Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
3. Under General Settings, click the button {% icon classes="fas fa-share-alt" /%} next to Manage Access.
4. Input the reader's e-mail address and expiry, if any.
5. Click Grant Access.

Once you click Grant Access, an e-mail message with be sent out to the e-mail address containing the magic link for access.

## How to Revoke Reader Access?

To revoke reader access:

1. From the sidebar, choose Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
2. Under General Settings, click the button {% icon classes="fas fa-share-alt" /%} next to Manage Access.
3. Find the reader whose access is to be revoked, then click on the {% icon classes="fas fa-times red-text" /%} next to it.

The reader will no longer be able to access the docs, or to request a magic link.

## Email Invite Customisation

If you would like to change the message that shows in red when a reader's email address is not registered, then please [contact us](/support-center/contact-us) with the exact message you would like to show. An example message would be:

"This e-mail address does not have an invitation. If you would like to get access, please email [elon@tesla.com](mailto:elon@tesla.com)"

The message can be designed using HTML as well.

## Email Invite API

You can also invite reader programmatically using our API. See:

- [Get access details of all invited readers](/v1.0/api/ref#get-reader-access)
- [Grant access to reader](/v1.0/api/ref#create-reader-access)
- [Revoke access to reader](/v1.0/api/ref#revoke-reader-access)

## Troubleshooting

If you are getting `Magic Link has already been used` everytime, it might be that an e-mail security software is installed on our mail domain. Such security software might access links to check it before you receive the e-mail, which causes the link to become void. Please [contact us](/support-center/contact-us) to resolve this mentioning "two step magic links".