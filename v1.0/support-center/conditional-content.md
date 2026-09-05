---
type: page
title: Conditional Content
listed: true
description: 
index_title: Conditional Content
hidden: false
keywords: 
tags: 
---

Conditional Content lets you control who can see specific content in your documentation based on user variables. Content visibility is managed through audiences, which define conditions that are evaluated against [variables](variables.md) passed in a signed JWT. This works on a private project through [custom login](private-docs/custom-login.md), and on a public docs site through a signed link.

{% synced id="beta-feature" /%}

There are two ways to use Conditional Content:

- **Page-level Audiences**: Apply an audience to an entire page to control who can access it.
- [**Conditional Blocks**](conditional-blocks.md): Use conditional blocks to control visibility of specific content within a page.

Both methods use the same audience system and conditions.

## Managing Audiences

Audiences are created and managed in Project Settings. Each audience has an ID and a set of conditions that determine when content is visible.

### Creating an Audience

To create a new audience:

1. Open Project Settings → **Content** → **Audiences**.
2. Click **Create audience**.
3. Enter an **Audience ID** (this ID will be used to reference the audience). It must start with a lowercase letter, and can contain only lowercase letters, numbers and hyphens.
4. Click **Save**.

### Editing Audience Conditions

To edit the conditions for an audience:

1. In Project Settings → Audiences, find the audience you want to edit.
2. Click on the menu {% icon classes="fas fa-ellipsis-v" /%} next to the audience.
3. Select **Edit**.
4. Use the expression builder to add or modify conditions.

In the expression builder, you can add as many conditions as needed. Each condition checks that a variable matches a value. All conditions must be satisfied for the content to show.

{% image url="../../assets/3b731ff238faf45d271cbd0a6a9fb5c8341e9dbd.png" /%}

### Deleting an Audience

To delete an audience:

1. In Project Settings → Audiences, find the audience you want to delete.
2. Click on the menu {% icon classes="fas fa-ellipsis-v" /%} next to the audience.
3. Select **Delete**.

{% callout type="warning" title="Deleting Audiences" %}
If an audience is in use on pages or conditional blocks, deleting it may affect content visibility.
{% /callout %}

## Setting Page Audience

You can apply an audience to an entire page to control who can access it. Page audiences are hierarchical, meaning child pages inherit their parent's audience automatically.

### Applying an Audience to a Page

To set an audience on a page:

1. Open the page you want to restrict.
2. In the right sidebar, open **Page Info** {% icon classes="fas fa-info-circle" /%} and go to the **Settings** tab.
3. Under **Audience**, select an audience from the dropdown.
4. The page will now only be visible to readers who match the audience conditions.

By default, all pages have their audience set to **public**, meaning they are visible to everyone.

### Audience Indicator

When a page has an audience set on it, editors will see a lock icon {% icon classes="fas fa-lock" /%} next to the page title in the index, indicating that the page has restricted access.

## Conditional Blocks

[Conditional blocks](conditional-blocks.md) allow you to control the visibility of specific content within a page. Each conditional block is assigned an audience.

To change the audience of a conditional block, click on the audience label (shown with a grey background) at the top of the block and select from the available audiences.

Learn more about using [Conditional Blocks](conditional-blocks.md).

## How Audiences are Evaluated

When a reader accesses your documentation, their audience is determined by matching the variables in their JWT token against the audience conditions.

Variables are passed through the `vars` object in the JWT payload when using [custom login](private-docs/custom-login.md). For example:

{% code %}
```javascript
const payload = {
  version: 1,
  vars: {
    userId: 1234,
    plan: "enterprise",
    region: "us"
  }
};
```
{% /code %}

These variables are then matched against the conditions defined in each audience to determine which content the reader can access.

### Identifying Readers on a Public Docs Site

Audiences are not limited to private documentation. A public docs site can identify a reader from a signed link, so you can tailor what each reader sees without putting your documentation behind a login.

Your Access method stays **Public**. The only thing you need to set up is an [API Key](project-settings/api-key.md) with the `access.write` **Modify access rules** permission, which is the key your token is signed with.

To identify a reader:

1. Sign a JWT in your backend exactly as you would for [custom login](private-docs/custom-login.md), putting the reader's details in the `vars` object. An expiry is required.
2. Send the reader to your docs site with the token in a `jwt` query parameter, for example `https://docs.pied-piper.com/getting-started?jwt=<token>`.
3. Your docs site verifies the token, applies the audiences the reader matches, and removes the token from the URL.

A reader who arrives with no token, or with one that has expired or cannot be verified, is not sent to a login screen. They see the public documentation, which is everything you have not assigned to an audience.

{% callout type="warning" title="Only a signed token sets audiences" %}
Variables injected through the `vars` and `hvars` query parameters or the `vars` cookie personalise text, but they do not put a reader into an audience. A reader can change them, so they can never unlock audience-gated content. Sign a JWT for anything you need to restrict.
{% /callout %}

{% callout title="Things to know" %}
- Link to a page inside your docs base path. If your documentation is served at `pied-piper.com/docs`, a link to `pied-piper.com/?jwt=...` sends the reader to `/docs` and the rest of the path is lost.
- A reader who has already been identified is not identified again until their token expires. Sending a new link with different variables has no effect while the previous one is still valid, so prefer short expiries.
- The **Generate JWT** button in Project Settings → Access is only available when the Access method is JWT, so sign your test tokens yourself.
- `error_redirect_url` has no effect on a public project, as there is no error screen to redirect from.
{% /callout %}

## Audiences and Search

Search results are filtered based on the reader's audience. Readers will only see search results for pages and content they have access to, ensuring that restricted content remains hidden even in search.

[AI Assistant](writing-documentation/ai-search.md) answers the same way. It draws on the documentation the reader is entitled to see, so an identified reader can ask about audience-gated content and find it, while an unidentified reader is answered from the public documentation alone.

If you require more of the Conditional Content feature, please do not hesitate to [contact us](contact-us.md).
