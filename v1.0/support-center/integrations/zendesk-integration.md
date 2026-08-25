---
type: page
title: Zendesk
listed: true
description: 
index_title: Zendesk
hidden: false
keywords: 
tags: 
---

Zendesk works with %product% in both directions. Our **DeveloperHub Docs** app puts your published documentation inside a Zendesk ticket, and the Zendesk Web Widget puts Zendesk support on your published documentation.

To bring your Zendesk help centre articles into %product% in the first place, see [Import from Zendesk](../importing-documentation/import-from-zendesk.md).

## Zendesk App

**DeveloperHub Docs** is our app for Zendesk Support. It adds a panel to the ticket sidebar where your agents search your published documentation and drop a link to the matching page straight into their reply.

Agents stop hunting through your documentation in another tab and pasting addresses by hand. Each link points at the exact heading that matched, so your customer lands on the answer rather than the top of a long page.

Install it from the [Zendesk Marketplace](https://www.zendesk.com/marketplace/apps/support/1281021/developerhub-docs/).

{% image url="./zendesk-app-sidebar.png" %}
The DeveloperHub Docs panel, searching from inside a ticket
{% /image %}

### Before You Start

You need:

- A Zendesk administrator account. Only administrators can install apps.
- A %product% project with [published](../publishing-documentation.md) documentation. The app searches published content only, so drafts and unpublished versions never appear.
- A [plan](https://developerhub.io/pricing) that includes the search API. [Contact us](../contact-us.md) if you are not sure.

### Creating an API Key

The app searches using an [API key](../project-settings/api-key.md), and that key also decides which project is searched. Create it in the project whose documentation your agents should see.

1. Open Project Settings → **API Keys**.
2. Create a new key, and give it a name that makes its purpose obvious, such as `Zendesk app`.
3. Under permissions, enable **Search** → **Query the search API**, and nothing else. A key limited to search cannot read or change anything else in your project.
4. Save the key, then copy it.

### Installing the App

1. In Zendesk, open **Admin Center**.
2. Go to **Apps and integrations** → **Apps** → **Zendesk Support apps**.
3. Click **Marketplace**, and search for **DeveloperHub Docs**.
4. Open the listing, and click **Install**.

Zendesk shows the settings form as soon as the install finishes. You can come back to it later from the app's **Settings** in Admin Center.

| Setting | What to enter |
| --- | --- |
| **DeveloperHub API key** | The key you copied above. |
| **Documentation version** | `latest` searches your default published version, and suits most teams. Enter a version slug such as `v2` to pin your agents to one version, or leave the field blank to search every published version. |
| **Link format** | `rich` inserts a clickable hyperlink, and is the right choice for most teams. Use `markdown` if your agents write their replies in Markdown, or `url` for the bare address. |

The same screen limits the panel to certain agent roles or groups, under **Enable role restrictions** and **Enable group restrictions**.

Click **Install** (or **Update**) to save.

{% callout title="Info" %}
One installation searches one project. To cover several products with separate documentation, install the app once per project, each with its own API key. Name each installation clearly, since your agents see all of them in the sidebar.
{% /callout %}

### Searching from a Ticket

Open any ticket, and find the **DeveloperHub Docs** panel in the right-hand sidebar. Type at least two characters; results appear as you type.

Each result names the heading that matched, the documentation section and page it sits on, its version, and a snippet with your agent's search terms highlighted. From there:

- Click a **result title** to open that page in a new browser tab, and check it before sending.
- Click **Insert link** to add a link to it to the reply being written.

{% image url="./zendesk-app-insert-link.png" %}
Insert link adds the link to the end of the open reply
{% /image %}

{% callout title="Info" %}
Zendesk only accepts inserted content at the end of an open reply, so write your message first and add your links after it. If you need a link mid sentence, move it once it is in.
{% /callout %}

### What Leaves Zendesk

- Only what an agent types into the search box is sent to %product%. Ticket content, requester details and agent identity never leave Zendesk, and the app stores nothing of its own.
- Your API key is held by Zendesk as a secure setting and added to each search on Zendesk's servers, so it never reaches the agent's browser and cannot be read from it.
- The key grants search and nothing else. It cannot read, change or publish your documentation, and revoking it in %product% stops the app immediately.

### Troubleshooting

| Message | What to do |
| --- | --- |
| DeveloperHub rejected the API key. | The key is wrong, has been revoked, or lacks the search permission. Create a new one with **Query the search API** enabled, and paste it into the app settings. |
| The search API is not available on this project's plan. | Your plan does not include the search API. [Contact us](../contact-us.md) to have it enabled. |
| No matching pages found, for something you know is documented. | Check the **Documentation version** setting: a version that does not contain the page cannot return it. Setting it to `latest`, or clearing it to search every version, confirms this quickly. Check also that the page is published, since drafts are never searched. |
| Could not add the link. Open a reply on this ticket, then try again. | Zendesk accepts inserted content only while a reply is open. Click into the comment box, then use **Insert link** again. |
| Too many searches in a short time. | The search API allows a high but finite number of requests per hour across your account. Wait a minute and try again. |

If the panel is blank, reload the ticket. If it stays blank, confirm in Admin Center that the app is installed, and that your role and group are not excluded by a role or group restriction.

## Zendesk Web Widget

The Zendesk Web Widget puts Zendesk support on your published documentation. To add it, you must have a [plan](https://developerhub.io/pricing) with [Custom HEAD Tags](../custom-javascript.md) enabled.

{% image url="https://uploads.developerhub.io/prod/02/zkmmo5ydr7dkvau0f6oxczi2x4qlloc4ngseyrdrmdftzyfv7zbnu35bs1r5r4v4.png" /%}

### Setting up Zendesk Web Widget

Follow the steps as provided in [Quickstart - Web Widget (Classic) APIs](https://developer.zendesk.com/documentation/classic-web-widget-sdks/web-widget/quickstart-tutorials/web-widget-javascript-apis/). Add the following [Custom HEAD Tag](../custom-javascript.md) replacing `YOUR_SNIPPET_KEY` with your own key:

{% code %}
```markup {% title="Custom HEAD Tag" %}
<!-- Start of Zendesk Widget script -->
<script id="ze-snippet" src="https://static.zdassets.com/ekr/snippet.js?key=YOUR_SNIPPET_KEY">
</script>
<!-- End of Zendesk Widget script -->
```
{% /code %}
