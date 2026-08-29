---
type: page
title: Organisation Settings
listed: true
description: Organisation Settings covers what applies across all of your projects: team members, usage statistics, shared customisation and SSO status.
index_title: Organisation Settings
hidden: false
keywords: 
tags: 
---

An organisation groups several projects, and the people who work on them, under a single owner. It is what makes organisation-wide SSO, shared styling and cross-project team management possible.

Organisations are set up by %product% rather than created from the editor. If you would like your projects grouped under one, [contact us](contact-us.md).

## Opening Organisation Settings

To open Organisation Settings, open the user menu in the editor top navigation and choose **Organisation settings**. Only the organisation owner sees this option.

You can also press {% key key="⌘" /%}/{% key key="Ctrl" /%} + {% key key="K" /%} and type the name of the pane you're looking for.

## Settings Groups

Organisation Settings is organised into groups. Each group contains panes:

- **People**: [Team](organisation-settings.md#team). Everyone in the organisation, and whether they can sign in.
- **Usage**: [Statistics](organisation-settings.md#statistics). User and project counts over the last three months.
- **Audit**: [Activity log](organisation-settings.md#activity-log). Every audited action across the projects your organisation owns.
- **Customisation**: [Custom CSS](organisation-settings.md#custom-css), [Custom HEAD tags](organisation-settings.md#custom-head-tags) and [Custom Footer](organisation-settings.md#custom-footer). Styling, head tags and a footer shared across projects that opt in.
- **Single Sign-On**: [SSO status](organisation-settings.md#sso-status). A read-only summary of your SSO configuration.

Managing members is limited to the organisation owner.

## Team

Organisation Settings → **Team** lists everyone in your organisation. Each member shows their name, e-mail address, when they were last active, and a status of **Owner**, **Active** or **Disabled**.

Use the search box to filter by name or e-mail address. Use **Sort by** to order the list by **Last active** or **Name**.

"Last active" is the last time the member opened %product%.

### Disabling a Member

Disabling a member keeps their account and all of their work, but stops them getting in. It is the right choice when someone leaves a team temporarily, or when you want to cut access without losing the history attributed to them.

To disable a member:

- Open Organisation Settings → **Team**.
- Click the chevron at the end of the member's row and choose **Disable member**.
- Confirm your choice.

Access is revoked immediately. Any sessions they have open end straight away, and they cannot log back in by any method, including SSO and passwordless login. They will see the message "Your account has been disabled. Please contact your organisation administrator."

Everything else is preserved: their account, name, e-mail address and project memberships stay as they are, so [page history](page-history.md) and the [activity log](activity-log.md) keep attributing past work to them.

The organisation owner cannot be disabled.

### Re-enabling a Member

To re-enable a member, click the chevron at the end of their row and choose **Enable member**. This takes effect straight away with no confirmation step. They keep the same account and the same project access they had before, and simply log in again.

Disabling and re-enabling a member are both recorded in the [activity log](activity-log.md) of every organisation project that member belongs to.

### Disable or Deprovision?

Both actions are on the same menu, and they are very different:

{% table layout="auto" %}
{% row %}
{% cell header=true %}
{% p /%}
{% /cell %}
{% cell header=true %}
Disable member
{% /cell %}
{% cell header=true %}
Deprovision from organisation
{% /cell %}
{% /row %}
{% row %}
{% cell %}
Can be undone
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
Keeps their user account
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
Keeps their project access for later
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
Stops them signing in again
{% /cell %}
{% cell %}
✅
{% /cell %}
{% cell %}
❌
{% /cell %}
{% /row %}
{% /table %}

Disabling is the only one of the two that keeps someone out. A disabled member is refused on every login route, including SSO.

Deprovisioning deletes the account, but it does not stop the person signing in again. Deprovisioning is only available on organisations that use SSO, so the next time they authenticate through your identity provider they are treated as somebody new and an account is created for them. Where your SSO connection adds users to all projects by default, they regain access immediately.

{% callout type="warning" title="Remove them from your identity provider first" %}
Deprovisioning on its own does not end access for someone who can still authenticate with your IdP. Revoke their access in your IdP, then deprovision. To stop someone signing in without touching your IdP, disable them instead.
{% /callout %}

For what deprovisioning removes, see [Deprovisioning Users](editor-single-sign-on--sso-.md#deprovisioning-users). It cannot be undone.

## Statistics

Organisation Settings → **Statistics** charts how your organisation has grown over the last three months:

- **Users**: the number of people with access to the organisation's projects, shown alongside **Active users**, meaning those who used %product% in the last 30 days.
- **Projects**: the number of projects in the organisation.

The charts are built from weekly snapshots, so a change you make today appears in the next snapshot rather than straight away.

## Activity log

Organisation Settings → **Activity log** gathers the [activity log](activity-log.md) of every project your organisation owns into one searchable trail. Where a project's own activity log answers "what happened in this project", this one answers "what happened anywhere in the organisation, and who did it".

Only the organisation owner can read it. It spans projects the owner may not administer individually, which is why it is not open to the admins of a single project.

Each entry shows what happened, the person or API key behind it, the project, the time, and the IP address the request came from.

To narrow the list:

- **Search** by user, project, action, or IP address.
- **Filter by project** using the project dropdown, or leave it on **All projects**. Projects that have since been deleted are still listed, marked as deleted.
- **Choose a scope** from the tabs across the top: **All**, **Content**, **Users**, **Security**, **Hosting**, **Plan**, and **Other**. Each tab carries a count of the entries it holds.

Use **Clear** to drop all of the filters at once. Entries are paged 25 at a time.

Entries survive the thing they describe. Deleting a project does not remove its history from this log, so the trail stays complete.

## Customisation

The **Customisation** group holds three things an organisation can publish for its projects to share: **Custom CSS**, **Custom HEAD tags** and **Custom Footer**. Only the organisation owner can edit them. Click **Save changes** to apply, or **Discard** to revert. There is no draft step here, so saving reaches every project that has opted in.

No project inherits any of them automatically. To opt one in, open Project Settings → **Customisation** and turn on **Use organisation CSS**, **Use organisation HEAD tags** or **Use organisation footer**. Only the project's owner can set these toggles.

If the organisation has not written anything yet, turning a toggle on changes nothing and the project keeps what it had.

### Custom CSS

One stylesheet shared across the organisation. The organisation stylesheet is applied first and the project's own [Custom CSS](customising-visuals/custom-css.md) after it, so a project rule wins over an organisation rule of equal specificity. It applies to the published docs and to the editor.

### Custom HEAD tags

The scripts, styles, meta and link tags injected into the page head across the organisation, such as analytics, site verification or a shared font. They are injected before the project's own [HEAD tags](custom-javascript.md), so where both set the same thing, the project's wins.

### Custom Footer

One footer, written as HTML in the same way as a project's [Custom Footer](customising-visuals/custom-footer.md). It is rendered in place of the project's own footer rather than alongside it, so a project that has written its own stops showing it while the toggle is on.

## SSO status

Organisation Settings → **SSO status** shows a read-only summary of your [SSO configuration](editor-single-sign-on--sso-.md#configuration):

- **SSO status**: whether an SSO provider is set up for the organisation.
- **Enforce SSO login**: whether users must sign in through the provider.
- **Default access to all projects**: whether new editors are added to every project by default.

To change any of these, [contact us](contact-us.md).

## Related

- [Collaboration](collaboration.md) for project-level teammates and [user roles](collaboration.md#user-roles).
- [Editor Single Sign-On (SSO)](editor-single-sign-on--sso-.md) for signing your team in through your identity provider.
