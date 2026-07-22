---
type: page
title: Private Documentation
listed: true
description: 
index_title: Private Documentation
hidden: false
keywords: visitor auth, visitor authentication, guest authentication, guest auth
tags: 
---

Supercharged plans admins can set their documentation portal as private, disallowing everyone on the internet to be able to access it. The protected project can be viewed by:

- Visiting the documentation site, and entering a [shared password](private-docs.md#password-protect-set-up).
- Opening a [shared link](private-docs.md#link-sharing).
- Invited readers through [magic links](private-docs/email-invite.md).
- [Custom login](private-docs/custom-login.md) flow using JSON Web Tokens (JWT).
- Single-Sign On (SSO).

If you are on an enterprise plan, then we also provide reader authentication through your intranet.

## Comparison Between Different Methods

{% table layout="auto" %}
{% row %}
{% cell header=true %}
Method
{% /cell %}
{% cell header=true %}
Security Level
{% /cell %}
{% cell header=true %}
Ease of Access
{% /cell %}
{% cell header=true %}
Needs a Developer?
{% /cell %}
{% cell header=true %}
Usage
{% /cell %}
{% /row %}
{% row %}
{% cell %}
[Password](private-docs.md#password-protect-set-up)
{% /cell %}
{% cell %}
Weak. Your readers might leak the password.
{% /cell %}
{% cell %}
Need to remember a password
{% /cell %}
{% cell %}
No
{% /cell %}
{% cell %}
Use to block out competitors and crawlers.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
[Shared Link](private-docs.md#link-sharing)
{% /cell %}
{% cell %}
Weak. Your readers might leak the link.
{% /cell %}
{% cell %}
Easy, click on a link.
{% /cell %}
{% cell %}
No
{% /cell %}
{% cell %}
Use to block out competitors and crawlers.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
[Reader Magic Link](private-docs/email-invite.md)
{% /cell %}
{% cell %}
Strong
{% /cell %}
{% cell %}
Easy, readers goes to the docs site, requests a magic link and opens the link.
{% /cell %}
{% cell %}
No
{% /cell %}
{% cell %}
Use to secure data and control access.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
[Custom Login](private-docs/custom-login.md)
{% /cell %}
{% cell %}
Strong
{% /cell %}
{% cell %}
Easy, reader needs to go to the docs site, but might need to log into your own site.
{% /cell %}
{% cell %}
Yes
{% /cell %}
{% cell %}
Use to secure data, control access and [personalise](personalised-docs.md) docs.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
[Single-Sign On (SSO)](private-docs/reader-single-sign-on.md)
{% /cell %}
{% cell %}
Strong
{% /cell %}
{% cell %}
Easy, reader needs to go to the docs site, but might need to log into SSO.
{% /cell %}
{% cell %}
No
{% /cell %}
{% cell %}
Use to secure data and control access.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Intranet (Enterprise only)
{% /cell %}
{% cell %}
Strong
{% /cell %}
{% cell %}
Easy, reader just needs to go to the docs site.
{% /cell %}
{% cell %}
Yes
{% /cell %}
{% cell %}
Use to secure data and control access.
{% /cell %}
{% /row %}
{% /table %}

## Password Protect Set up

To set up password protection:

- Open Project Settings → **Access**.
- In the Access method card, select **Password**.

{% image url="https://uploads.developerhub.io/prod/02/3op6frix1y6b0iu6ie8vw3zt4lp1rebppslm1w5o3b019kin8xi96snr3gpc705r.png" width=448 /%}

- Input the password.
- Click **Save changes** in the top menu.

{% image url="https://uploads.developerhub.io/prod/02/nzlxbav839gbvtovl93bd2i68iam72yp2btk9a3l2olwgupwottbp9h4rdltiqr5.png" /%}

{% callout type="success" title="Success" %}
Great, all the published pages of this project are now protected by a password
{% /callout %}

To try it out, go to the live mode of your documentation. You will be presented with such a page.

{% image url="https://uploads.developerhub.io/prod/02/ttjhjrm2tptigmzb9kkvpo42j1ihfafg4qhv4yz4kzbus123ww4clk40fm9wrmyd.jpg" /%}

Once a reader inputs the right password, they will continue to be logged in for 24 hours.

{% callout type="warning" title="Warning" %}
You should not save confidential or sensitive information in a password protected project. This is to prevent the general public and search engines from accessing your pages rather than to secure data.
{% /callout %}

## Link Sharing

Once a project is protected by a password, you can share a link which accesses the project without the need to enter a password. You can use this feature to provide only your customers with read access by sharing this link internally with them.

To share a link:

- Open Project Settings → **Access**.
- In the Sharing \& invites card, click **Share link**.

{% image url="https://uploads.developerhub.io/prod/02/w2f0pq7konhpbfcklasx822gsqd750c96j63hry3od99cybni0zl3jcigvrw5qv7.png" width=478 /%}

- You can send invitations directly to your readers. Separate e-mail address by using commas.
- Or you can copy the link and paste it.

{% callout type="warning" title="Warning" %}
The link will be revoked once the password changes or is removed.
{% /callout %}

## Using Login URL

If your docs are protected by using a [shared link](private-docs.md#link-sharing) or a [custom login flow](private-docs/custom-login.md), then your readers probably need to authenticate with your own website first, and you need to provide them with a URL that allows them to authenticate on your docs. Thus, we can make this easier by redirecting your unauthenticated readers to a URL which you specify, where:

- If you are using secure link sharing, it would take them to the page where they can find the link, or the page that redirects them to the link if they're authenticated on your own website.
- If you are using [custom login](private-docs/custom-login.md), it would take them to an authentication page which if they are already logged in to your own website, then it just redirects back with a valid URL to the docs site, otherwise would prompt them to log in first.

To setup login URL:

- Open Project Settings → **Access**.
- Under Login URL, input the URL. An example would be `https://pied-piper.com/docs-login`.
- Click **Save changes** in the top menu.

### Disabling Protection

To disable password protection:

- Open Project Settings → **Access**.
- In the Access method card, choose **Public** {% icon classes="fas fa-unlock" /%}.
- Click **Save changes** in the top menu.

The project will then be unprotected.

{% callout type="warning" title="Warning" %}
All your published versions will continue to be published. Make sure to unpublish any version that you do not want accessible to the general public before you unprotect the project if needed.
{% /callout %}
