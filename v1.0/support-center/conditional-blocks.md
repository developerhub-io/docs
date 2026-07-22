---
type: page
title: Conditional Blocks
listed: true
description: 
index_title: Conditional Blocks
hidden: false
keywords: 
tags: 
---

Conditional blocks let you control who can see a given block of content on your page based on content audiences. Audiences define conditions that determine whether content is visible to specific readers.

{% synced id="beta-feature" /%}

## Create a Conditional Block

To add a conditional block:

{% synced id="open-block-menu" /%}

- Select **Conditional Block**.
- Add the content as needed inside the conditional block.
- The block will be assigned a default audience.

## Setting the Audience

Each conditional block uses an audience to determine visibility. To change the audience:

- Click on the audience label (shown with a grey background) at the top of the conditional block.
- Select from the dropdown of available audiences.

Audiences are managed in [Project Settings](project-settings.md). Learn more about creating and configuring audiences in [Conditional Content](conditional-content.md).

## How Audiences are Evaluated

When a reader views your documentation, their audience is evaluated based on variables passed through [custom login](private-docs/custom-login.md). The `vars` object in the JWT payload is matched against the audience conditions to determine which conditional blocks are visible.

{% callout title="Managing Audiences" %}
To create, edit, or delete audiences, go to Project Settings → Audiences. See [Conditional Content](conditional-content.md) for full details.
{% /callout %}

If you require more of the Conditional Content feature, please do not hesitate to [contact us](contact-us.md).
