---
type: page
title: Project Settings
listed: true
description: Learn how to access and change project settings including project details, hosting, security, and more. Also, find out how to change the title and website link, set privacy policy consent, and enable automatic saving.
index_title: Project Settings
hidden: false
keywords: 
tags: 
---

Project Settings is a full page where you change [hosting](hosting.md), [customisation](customising-visuals.md), [security](private-docs.md), [team](collaboration.md), plan and other details.

## Opening Project Settings

To open Project Settings:

- In the editor top navigation, click on the project menu.
- Click the settings {% icon classes="fas fa-cog" /%} cog.

You can also press {% key key="⌘" /%}/{% key key="Ctrl" /%} + {% key key="K" /%} and type the name of the setting you're looking for.

## Settings Groups

Project Settings is organised into groups. Each group contains panes:

- **General**: Project title, project ID, privacy policy URL, move content, delete project.
- **Insights**: Dashboard view (activity, drafts, comments, feedback).
- **Hosting**: Subdomain, custom domain, base path, SSL, search-engine indexing, redirects, server headers.
- **Customisation**: Logo, favicon, top navigation links, colours, font, theme, [Custom CSS](customising-visuals/custom-css.md), [Custom Footer](customising-visuals/custom-footer.md), [HEAD tags](custom-javascript.md).
- **Access**: [Password](private-docs.md#password-protect-set-up), [email](private-docs/email-invite.md), [SSO](private-docs/reader-single-sign-on.md) and [JWT](private-docs/custom-login.md) access.
- **Feedback**: [Reader feedback and AI moderation](feedback.md#feedback-settings).
- **Content**: [Glossary](glossary.md), [Navigation Groups](customising-visuals/top-navigation-bar.md#navigation-structure), [Project Variables](variables.md), [Page Tags](tags.md), [Audiences](conditional-content.md).
- **Developers**: [API Keys](project-settings/api-key.md), [Integrations](integrations.md) (Slack, GitHub, Intercom, Google Analytics), [Docs Sync](github-sync.md).
- **AI**: [AI Agents \& MCP](ai-features.md), [Self-Updating Docs](self-updating-docs.md).
- **Team**: [Invite teammates, change roles, transfer ownership](collaboration.md).
- **Plan \& Usage**: Current plan, seats, [upgrade](supercharged-plans.md).
- **Advanced**: Editorial flow toggles, pinned deployment, multi-format exports.

{% callout title="Saving changes" %}
Most settings in Project Settings use a draft model. Edit the controls you want, then click **Save changes** in the top menu to commit. **Discard** reverts your draft. Images (logo, favicon) are an exception; they save automatically on upload.
{% /callout %}

## Changing Title

The title shows in the browser tab title.

To change the title:

1. Open Project Settings.
2. Under **General**, edit Project title.
3. Click **Save changes** in the top menu.

## Changing Website Link

The logo link is the URL your readers are navigated to on clicking the project logo on the published docs.

To change the logo link:

1. Open Project Settings.
2. Under **Customisation**, find the Brand assets card.
3. Edit Logo link URL.
4. Click **Save changes** in the top menu.

{% callout title="Info" %}
If the link is not set, then the user will be navigated to the landing page (if enabled).
{% /callout %}

## Privacy Policy Consent

If you are setting cookies on your documentation portal, then you will need to ask for the user's consent. If you provide a privacy policy URL in your project settings, then we will show our own privacy policy consent which will prevent our [Google Analytics](integrations/google-analytics.md) integration from tracking your users until they accept the cookie consent.

To set your own privacy policy:

1. Open Project Settings.
2. Under **General**, edit Privacy policy URL.
3. Click **Save changes** in the top menu.
