---
type: page
title: Collaboration
listed: true
slug: collaboration
description: Learn how to collaborate efficiently with your teammates. Discover the different user roles and their permissions. Invite and remove teammates easily, and even transfer project ownership if needed.
index_title: Collaboration
hidden: 
keywords: 
tags: 
---

Supercharged plan users can collaborate with their teammates on [reviewing](/support-center/comments) and writing documentation. Teammates can have different [roles](/support-center/collaboration#user-roles).

## User Roles

Each teammate can have one of the four user roles that we support. The roles are - in the order of most authoritative to least:

- **Admin**, where **Owner** is always an admin.
- **Publisher**
- **Writer**
- **Reviewer**

A breakdown of the permissions is detailed below:

{% table %}
| Role | Admin | Publisher | Writer | Reviewer | 
| ---- | ---- | ---- | ---- | ---- | 
| Read draft and published pages | ✅ | ✅ | ✅ | ✅ | 
| See page history | ✅ | ✅ | ✅ | ✅ | 
| Comment on pages | ✅ | ✅ | ✅ | ✅ | 
| View teammates | ✅ | ✅ | ✅ | ✅ | 
| Download PDF export | ✅ | ✅ | ✅ | ✅ | 
| Create/edit page drafts | ✅ | ✅ | ✅ | ❌ | 
| Create/edit API references drafts | ✅ | ✅ | ✅ | ❌ | 
| Create [synced blocks](/support-center/synced-blocks) | ✅ | ✅ | ✅ | ❌ | 
| Create unpublished documentation section | ✅ | ✅ | ✅ | ❌ | 
| Delete pages | ✅ | ✅ | ❌ | ❌ | 
| Create/delete/publish versions | ✅ | ✅ | ❌ | ❌ | 
| Publish/delete documentation sections | ✅ | ✅ | ❌ | ❌ | 
| Publish/delete API references | ✅ | ✅ | ❌ | ❌ | 
| Modify documentation, API references and versions settings | ✅ | ✅ | ❌ | ❌ | 
| Edit/archive [synced blocks](/support-center/synced-blocks) | ✅ | ✅ | ❌ | ❌ | 
| Publish pages | ✅ | ✅ | ❌ | ❌ | 
| Import/export project | ✅ | ✅ | ❌ | ❌ | 
| Generate PDF export/permalink | ✅ | ✅ | ❌ | ❌ | 
| Change project variables | ✅ | ✅ | ❌ | ❌ | 
| Lock/unlock versions | ✅ | ✅ | ❌ | ❌ | 
| Change plan | ✅ | ✅ | ❌ | ❌ | 
| Manage teammates | ✅ | ❌ | ❌ | ❌ | 
| Change project settings | ✅ | ❌ | ❌ | ❌ | 
| Create/view/revoke API key | ✅ | ❌ | ❌ | ❌ | 
| Delete project | Owner only | ❌ | ❌ | ❌ | 
{% /table %}

## Setting up Teammates

- If you are on a paid plan, you can invite your teammates to collaborate from the Team menu.
- Open the Team {% icon classes="fas fa-users-cog inv-icon" /%} menu from the sidebar.
- Click on "Invite teammate to collaborate" {% icon classes="fas fa-plus" /%}
- Enter the e-mail address of the teammate to invite. You can add multiple at the same time by separating them with a comma.
- If you want to change their role, click on their badge and change it.
- If you want to change their name, click on their badge and select "Edit Name".

If they are not already a user, an e-mail message will be sent to the e-mail address to help them sign up. They will be added in the list, and an "Invited" badge will be next to their e-mail address until they are signed up.

If they are already a user, an e-mail message will be sent to their e-mail address to notify them that they can collaborate on this project. They will be automatically added and no prompt is required from them.

{% image url="https://image-archive.developerhub.io/image/upload/1253/e5ol2cjcrgu1fxwni98j/1598785884.png" mode="responsive" height="532" width="618" %}
{% /image %}

## Remove a Teammate

To remove a teammate, do the following:

- Open the Team {% icon classes="fas fa-users-cog inv-icon" /%} menu from the sidebar.
- Click on the badge next to the user and select "Remove teammate".

If your organisation is managed (for Enterprise), check [Deprovisioning Users](/support-center/editor-single-sign-on--sso-#deprovisioning-users).

## Changing Project Ownership

To move ownership to another teammate:

1. Make sure that the user has been invited, has already joined the project as a teammate.
2. Open the Team {% icon classes="fas fa-users-cog inv-icon" /%} menu from the sidebar.
3. Click on the badge next to the user and select "Make Owner".
4. Confirm your choice. The user will receive an e-mail that they became an owner of the project.

{% callout type="warning" title="Transferring Ownership" %}
Once you transfer ownership, you cannot take it back unless if the new owner transfers it back to you.
{% /callout %}

{% callout type="info" title="Invoicing is not connected to ownership" %}
If you have a supercharged plan, then the invoice by default would be sent to the e-mail address of the user who purchased the plan, not the owner. If you wish to modify the e-mail used for receiving invoices, check [Changing Payment/Billing Details](/support-center/supercharged-plans#changing-paymentbilling-details).
{% /callout %}