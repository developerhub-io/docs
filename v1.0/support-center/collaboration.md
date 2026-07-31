---
type: page
title: Collaboration
listed: true
description: Learn how to collaborate efficiently with your teammates. Discover the different user roles and their permissions. Invite and remove teammates easily, and even transfer project ownership if needed.
index_title: Collaboration
hidden: false
keywords: 
tags: 
---

Supercharged plan users can collaborate with their teammates on [reviewing](comments.md) and writing documentation. Teammates can have different [roles](collaboration.md#user-roles).

## User Roles

Each teammate can have one of the four user roles that we support. The roles are - in the order of most authoritative to least:

- **Admin**, where **Owner** is always an admin.
- **Publisher**
- **Writer**
- **Reviewer**

A breakdown of the permissions is detailed below:

{% table layout="auto" %}
{% row %}
{% cell header=true %}
Role
{% /cell %}
{% cell header=true %}
Admin
{% /cell %}
{% cell header=true %}
Publisher
{% /cell %}
{% cell header=true %}
Writer
{% /cell %}
{% cell header=true %}
Reviewer
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Read draft and published pages
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% /row %}
{% row %}
{% cell %}
See page history
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Comment on pages
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% /row %}
{% row %}
{% cell %}
View teammates
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Download PDF export
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Create/edit page drafts
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Create/edit API references drafts
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Create [synced blocks](synced-blocks.md)
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Create unpublished documentation section
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Delete pages
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Create/delete/publish versions
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Publish/delete documentation sections
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Publish/delete API references
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Modify documentation, API references and versions settings
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Edit/archive [synced blocks](synced-blocks.md)
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Publish pages
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Import/export project
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Generate PDF export/permalink
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Change project variables
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Lock/unlock versions
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Change plan
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Manage teammates
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Change project settings
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Create/view/revoke API key
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Delete project
{% /cell %}
{% cell %}
Owner only
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% /table %}

## Setting up Teammates

If you are on a paid plan, you can invite your teammates to collaborate from the Team pane:

- Open Project Settings → **Team**. You can also open the user menu in the top navigation and choose **Invite teammates**.
- In the toolbar, enter the e-mail address of the teammate to invite and click **Invite**. You can add multiple at the same time by separating them with a comma.
- To change a teammate's role, use the role select next to their name.
- To change a teammate's display name, click their badge and select **Edit name**.

If they are not already a user, an e-mail message will be sent to the e-mail address to help them sign up. They will be added in the list, and an "Invited" badge will be next to their e-mail address until they are signed up.

If they are already a user, an e-mail message will be sent to their e-mail address to notify them that they can collaborate on this project. They will be automatically added and no prompt is required from them.

{% image url="https://uploads.developerhub.io/prod/02/fiw1hrnfsvas5rrl7930dplahylr601j9iv4wk11cykq6dpa92aggsrbg7420um9.png" /%}

## Remove a Teammate

To remove a teammate, do the following:

- Open Project Settings → **Team**.
- Click the badge next to the user and select **Remove teammate**.

This removes them from the project only.

{% callout title="Organisations" %}
If your projects are part of an organisation, the organisation owner can also **disable** a member from Organisation Settings → **Team**. Disabling blocks them from logging in to any project, but keeps their account and history, and can be undone. See [Organisation Settings](organisation-settings.md).
{% /callout %}

If your organisation is managed (for Enterprise), check [Deprovisioning Users](editor-single-sign-on--sso-.md#deprovisioning-users).

## Changing Project Ownership

To move ownership to another teammate:

1. Make sure that the user has been invited, has already joined the project as a teammate.
2. Open Project Settings → **Team**.
3. Click the badge next to the user and select **Make owner**.
4. Confirm your choice. The user will receive an e-mail that they became an owner of the project.

{% callout type="warning" title="Transferring Ownership" %}
Once you transfer ownership, you cannot take it back unless if the new owner transfers it back to you.
{% /callout %}

{% callout title="Invoicing is not connected to ownership" %}
If you have a supercharged plan, then the invoice by default would be sent to the e-mail address of the user who purchased the plan, not the owner. If you wish to modify the e-mail used for receiving invoices, check [Changing Payment/Billing Details](supercharged-plans.md#changing-paymentbilling-details).
{% /callout %}
