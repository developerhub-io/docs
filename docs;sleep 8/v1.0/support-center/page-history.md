---
type: page
title: Page History
listed: true
slug: page-history
description: 
index_title: Page History
hidden: 
keywords: 
tags: 
---

Supercharged plans can view and go back to older versions of each page.

{% image url="https://image-archive.developerhub.io/image/upload/v2_1/rrv8kcxakxzxbjqif6qb/1612105931.png" mode="responsive" height="985" width="1751" %}
{% /image %}

## View and Revert Edit History

To view edit history of a page:

- Select the page from the index.
- Select Page Info {% icon classes="fas fa-file-alt inv-icon" /%} from the right sidebar.
- Each edit will be shown in chronological order, newest (or current) first, supplied with the team member who made the changes, the local time, and an "estimate" of how many lines have been added or removed.
- On clicking on an edit history, the page will preview the change that was made.
- You may at this stage revert to this change. This will create a new edit history.

{% callout type="info" title="Info" %}
Users upgrading to a higher tier plan will be able to access history older than what their previous plan allowed immediately.
{% /callout %}

{% callout type="success" title="Behaviour when Cloning" %}
When you clone a version, the page history of the original page will be accessible on the cloned page - even if you delete the original version.
{% /callout %}

## Annotate History

To make it easier for your team to figure out the changes you made in an edit history, you may annotate (similar to adding a commit message) the change. To annotate a history:

- Select the page from the index.
- Select Page Info {% icon classes="fas fa-file-alt inv-icon" /%} from the right sidebar.
- Hover over the edit you wish to annotate, and click on the edit icon {% icon classes="fas fa-edit" /%} next to it.
- Type in your commit message and submit it.

## See Changes since Published Page

If you are currently writing a draft, and you need to review the changes since page was last published:

- Select the page from the index.
- Select Page Info {% icon classes="fas fa-file-alt inv-icon" /%} from the right sidebar.
- Next to Edit History, click on Compare With Published.

{% image url="https://image-archive.developerhub.io/image/upload/v2_1/jhlohkfins1clwbt5tkt/1612106730.png" mode="responsive" height="164" width="339" %}
{% /image %}

All edits since last published edit will be merged and showed.

## Known Limitations & Bugs

- Diffs might have extra spaces and dashes after an import.
- If a [block](/support-center/blocks) is changed, then we only highlight it in orange and we do not show the previous state. The new state is only shown.