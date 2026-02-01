---
type: page
title: Conditional Content
listed: true
slug: conditional-content
description: 
index_title: Conditional Content
hidden: 
keywords: 
tags: 
---

Conditional Content lets you control who can see specific content in your documentation based on user variables. Content visibility is managed through audiences, which define conditions that are evaluated against [variables](/support-center/variables) passed via [custom login](/support-center/custom-login).

{% synced id="beta-feature" %}
{% /synced %}

There are two ways to use Conditional Content:

- **Page-level Audiences**: Apply an audience to an entire page to control who can access it.
- **[Conditional Blocks](/support-center/conditional-blocks)**: Use conditional blocks to control visibility of specific content within a page.

Both methods use the same audience system and conditions.

## Managing Audiences

Audiences are created and managed in Project Settings. Each audience has an ID and a set of conditions that determine when content is visible.

### Creating an Audience

To create a new audience:

1. From the sidebar, choose Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
2. Navigate to **Audiences**.
3. Click **Create audience**.
4. Enter an **Audience ID** (this ID will be used to reference the audience).
5. Click **Save**.

### Editing Audience Conditions

To edit the conditions for an audience:

1. In Project Settings → Audiences, find the audience you want to edit.
2. Click on the menu {% icon classes="fas fa-ellipsis-v" /%} next to the audience.
3. Select **Edit**.
4. Use the expression builder to add or modify conditions.

In the expression builder, you can add as many conditions as needed. Each condition checks that a variable matches a value. All conditions must be satisfied for the content to show.

{% image url="asset:rotyylnr1119" mode="responsive" height="318" width="529" %}
{% /image %}

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
2. In the right sidebar, go to **Page Info**.
3. Under **Audience**, select an audience from the dropdown.
4. The page will now only be visible to readers who match the audience conditions.

By default, all pages have their audience set to **public**, meaning they are visible to everyone.

### Audience Indicator

When a page has an audience set on it, editors will see a lock icon {% icon classes="fas fa-lock" /%} next to the page title in the index, indicating that the page has restricted access.

## Conditional Blocks

[Conditional blocks](/support-center/conditional-blocks) allow you to control the visibility of specific content within a page. Each conditional block is assigned an audience.

To change the audience of a conditional block, click on the audience label (shown with a grey background) at the top of the block and select from the available audiences.

Learn more about using [Conditional Blocks](/support-center/conditional-blocks).

## How Audiences are Evaluated

When a reader accesses your documentation, their audience is determined by matching the variables in their JWT token against the audience conditions.

Variables are passed through the `vars` object in the JWT payload when using [custom login](/support-center/custom-login). For example:

{% code %}
{% tab language="javascript" %}
const payload = {
  version: 1,
  vars: {
    userId: 1234,
    plan: "enterprise",
    region: "us"
  }
};
{% /tab %}
{% /code %}

These variables are then matched against the conditions defined in each audience to determine which content the reader can access.

## Audiences and Search

Search results are filtered based on the reader's audience. Readers will only see search results for pages and content they have access to, ensuring that restricted content remains hidden even in search.

If you require more of the Conditional Content feature, please do not hesitate to [contact us](/support-center/contact-us).
