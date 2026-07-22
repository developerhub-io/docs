---
type: page
title: 2024 Updates
listed: true
description: 
index_title: 2024 Updates
hidden: false
keywords: 
tags: 
---

See [Upcoming Features](../upcoming-features.md) to know what we're currently working on.

## 2024 Updates

### 24 Dec

- {% badge text="New " type="success" /%} **Code Steps:** Add [code walkthroughs](../code-steps.md) to your documentation.

### 23 Dec

- {% badge text="Improvement" /%} **Editor**: Major improvement for pasting content.

### 18 Dec

- {% badge text="New" type="success" /%} **Developer Tools**: `onreferencecontentloaded` [event](../developer-tools.md#on-reference-content-loaded) available to modify API reference UI as needed.
- {% badge text="Improvement" /%} **API Playground**: Bearer would be added automatically to the request with bearer security scheme.

### 17 Dec

- {% badge text="Bug Fix" type="error" /%} **Tables**: Fix to deleting first column on a new table and setting columns widths.

### 16 Dec

- {% badge text="Improvement" /%} **Editor**: Pasting improvements for variables, glossary and links.

### 13 Dec

- {% badge text="New" type="success" /%} **API Reference**: `x-enum-varnames` now supported as an [OpenAPI extension](../api-references/openapi-extensions.md).

### 5 Dec

- {% badge text="New" type="success" /%} **GitHub Sync**: [Sync your docs](../github-sync.md) with GitHub.

### 3 Dec

- {% badge text="Bug Fix" type="error" /%} **API Reference**: Requests with `application/x-www-form-urlencoded` content type having special characters did not have them encoded.

### 28 Nov

- {% badge text="Bug Fix" type="error" /%} **API Playground**: Requests with `application/x-www-form-urlencoded` content type were handled as query string.

### 25 Nov

- {% badge text="New" type="success" /%} **Readability Metrics**: Right sidebar indicator for [readability](../readability-metrics.md) for English content.

### 13 Nov

- {% badge text="Improvement" /%} **API Reference**: Password OAuth2 flow type now accepts client authentication pair in the API playground.

### 11 Nov

- {% badge text="Improvement" /%} **API Reference**: Example requests and responses show summary in the select list instead of key.

### 25 Oct

- {% badge text="Improvement" /%} **Landing Page**: Variables written in default landing page layout would be rendered automatically.

### 24 Oct

- {% badge text="New" type="success" /%} **Landing Page**: Variables written in landing pages or custom pages would be rendered automatically.
- {% badge text="New" type="success" /%} **Custom Login**: `jti` parameter can be used to make a single JWT valid for only one device.
- {% badge text="Improvement" /%} **Feedback**: Further measures to block spam.
- {% badge text="Improvement" /%} **Feedback**: Can disable feedback using [advanced settings](../project-settings/advanced-settings.md) according to [referrer](../feedback.md#feedback-spam-filter).

### 22 Oct

- {% badge text="Bug Fix" type="error" /%} **Import**: Fix to project imports where page headers might show.

### 13 Oct

- {% badge text="New" type="success" /%} **Editor**: [Blocks](../writing-documentation/blocks.md) and inline blocks can now be added by typing {% key key="/" /%} anywhere.
- {% badge text="Improvement" /%} **Editor**: Several improvements to blocks to make it easier to edit docs completely using keyboard without having to move the cursor, as well as cosmetic enhancements.
- {% badge text="Improvement" /%} **AI Features**: All our AI features use the enhanced `gpt-4o-mini` model now.

### 8 Oct

- {% badge text="Bug Fix" type="error" /%} **Feedback**: Feedback chart used to fail to load in rare cases.
- {% badge text="Bug Fix" type="error" /%} **Feedback**: Long and unusual feedback messages could've broken the dashboard layout.

### 27 Sep

- {% badge text="New" type="success" /%} **Video**: Start a youtube video at a certain time.

### 24 Sep

- {% badge text="Improvement" /%} **General**: Upgraded our databases to the latest and greatest.
- {% badge text="Bug Fix" type="error" /%} **Export**: Non-standard characters now become underscores in exported file names.
- {% badge text="Bug Fix" type="error" /%} **Comments**: User selector was not opening every time when hitting `@` in the comments box.

### 18 Sep

- {% badge text="Improvement" /%} **API Reference**: Recognise `date` string format.

### 17 Sep

- {% badge text="Bug Fix" type="error" /%} **Editor**: Page options were making page wider if the page slug was too long.

### 15 Sep

- {% badge text="New" type="success" /%} **API Reference**: Support for `x-tagGroups` for tag grouping.
- {% badge text="Change" type="warning" /%} **Editor**: Editor toolbar has a new look.

### 14 Sep

- {% badge text="Improvement" /%} **UI Translation**: Added `search.ai.answer`.

### 9 Sep

- {% badge text="New" type="success" /%} **API Reference**: Deprecated fields in response schemas are now shown in strikethough format.

### 7 Sep

- {% badge text="Bug Fix" type="error" /%} **Synced Block**: Importing a page that has invalid synced block IDs was failing the import.

### 2 Sep

- {% badge text="New" type="success" /%} **Tables**: Ability to reorder columns and rows.

### 31 Aug

- {% badge text="Improvement" /%} **Inlines Images**: Further improvement to resizing images.

### 30 Aug

- {% badge text="New" type="success" /%} **Inline Images**: Fit width mode available to take 100% of container space.
- {% badge text="Improvement" /%} **SEO**: XML sitemaps are made default.
- {% badge text="Bug Fix" type="error" /%} **Search**: Organisation search was down.

### 29 Aug

- {% badge text="New" type="success" /%} **Inline Images**: [Inline Images](../inline-images.md) are now available in beta. Great for tables!

### 28 Aug

- {% badge text="New" type="success" /%} **Code block**: [Highlighting lines](../code-blocks.md#highlight-code) is now available.
- {% badge text="New" type="success" /%} **Code block**: A local setting to [show line numbers](../code-blocks.md#show-line-numbers) is available.
- {% badge text="Bug Fix" type="error" /%} **Search**: Some headings were unreachable due to different fragment links.
- {% badge text="Bug Fix" type="error" /%} **AI Search**: Logs were not downloading fully in certain situations.

### 27 Aug

- {% badge text="Improvement" /%} **Email Invite**: [Two step magic link](../private-docs/email-invite.md#troubleshooting) is available in case links are getting used by email security software.
- {% badge text="Bug Fix" type="error" /%} **Login**: A bug was introduced on 18 Aug which changed how we log in users. All users who have tried to log in since 18 Aug needed to reset their password. We have fixed that bug and old credentials are working again. Unfortunately, users who reset their passwords must change their passwords again.

### 26 Aug

- {% badge text="Bug Fix" type="error" /%} **Editor**: Instant markdown formatting was not showing in callouts.
- {% badge text="Bug Fix" type="error" /%} **Page Linking**: API reference operations were not showing if the API reference was not published yet.

### 22 Aug

- {% badge text="Bug Fix" type="error" /%} **SEO**: Sitemaps were erroring.

### 21 Aug

- {% badge text="Bug Fix" type="error" /%} **Email Invites**: Fixed error message when the invite is expired.

### 18 Aug

- {% badge text="Improvement" /%} **General**: We have huge infrastructure updates, we are all up to date!

### 14 Aug

- {% badge text="Bug Fix" type="error" /%} **Editor**: Pasting links in the links box did not have an effect.

### 13 Aug

- {% badge text="Bug Fix" type="error" /%} **Editor**: Pasting images inside list items was duplicating the image.

### 12 Aug

- {% badge text="Bug Fix" type="error" /%} **Editor**: Inline code formatting button on the toolbar was not working.

### 8 Aug

- {% badge text="New" type="success" /%} **Redirect**: Complete site redirects possible now by contacting us.

### 31 Jul

- {% badge text="Change" type="warning" /%} **API References**: Writers can [create and edit](../collaboration.md) API references in draft now.

### 24 Jul

- {% badge text="Improvement" /%} **AI Search**: Now using `gpt-4o-mini` model which provides more reasoning in the answers.

### 22 Jul

- {% badge text="Improvement" /%} **General**: We've had multiple performance improvements throughout the editor.
- {% badge text="Bug Fix" type="error" /%} **General**: Users in South Africa were unable to load the site due to an AWS failure.

### 18 Jul

- {% badge text="Bug Fix" type="error" /%} **API Reference**: Jumping to heading on first load was some pixels out of view.

### 8 Jul

- {% badge text="Change" type="warning" /%} **SEO**: Sitemaps are now generated every 6 hours.

### 6 Jul

- {% badge text="Change" type="warning" /%} **Custom Login**: JWTs can only be signed using an API Key that has `access.write` permission.
- {% badge text="Improvement" /%} **General**: We've updated our front-end libraries completely. Using the latest technology now!

### 26 Jun

- {% badge text="Bug Fix" type="error" /%} **Editor**: Formatting text using toolbar as inline code was not activating save button.

### 25 Jun

- {% badge text="New" type="success" /%} **Table**: Ability to duplicate rows and columns.

### 24 Jun

- {% badge text="Improvement" /%} **Search**: Many improvements and bug fixes for [AI Assistant](../using-search/ai-search.md).

### 23 Jun

- {% badge text="New" type="success" /%} **Page Linking**: Pages now have [permalinks](../writing-documentation/page-linking.md#page-permalinks).

### 22 Jun

- {% badge text="New" type="success" /%} **Search**: [AI Assistant](../using-search/ai-search.md) is now available for testing in beta for all grow and enterprise plans users.

### 5 Jun

- {% badge text="New" type="success" /%} **SSO**: Assign roles to users using attributes.
- {% badge text="Improvement" /%} **General**: User invites would default to the role set up for SSO, if set.

### 1 Jun

- {% badge text="Bug Fix" type="error" /%} **Github Code**: Markdown files were not styled correctly.

### 22 May

- {% badge text="New" type="success" /%} **Editors**: Grow plan projects can have more than 20 editors. See [pricing](https://developerhub.io/pricing).

### 18 May

- {% badge text="New" type="success" /%} **Search**: AI Search is now available in alpha.
- {% badge text="New" type="success" /%} **API**: [GET - Read reference](/v1.0/api/ref#read-reference) is now available.
- {% badge text="New" type="success" /%} **API**: [GET - Get all resources](/v1.0/api/ref#all-project) has two new query parameters `versionId` and `published`, and it provides `published` for all items.
- {% badge text="Improvement" /%} **API Reference**: Long response examples would be collapsed by default if possible.

### 14 May

- {% badge text="New " type="success" /%} **Find \& Replace**: Find and Replace now supports searching in Custom HTML blocks.
- {% badge text="New" type="success" /%} **API Reference**: New setting to only show request payload without code samples.

### 24 Apr

- {% badge text="New" type="success" /%} **Feedback**: Feedback can be [marked as spam](../feedback.md#where-can-i-find-the-received-feedback).
- {% badge text="New" type="success" /%} **Feedback**: Spam messages can be [filtered automatically](../feedback.md#feedback-spam-filter).
- {% badge text="New" type="success" /%} **Feedback**: Personal identifiable information can be [redacted automatically](../feedback.md#redact-pii-from-feedback).

### 22 Apr

- {% badge text="New" type="success" /%} **Team**: Writers can now re-arrange pages in index.
- {% badge text="New" type="success" /%} **General**: We will notify you when you're using an out-dated version of our site.

### 20 Apr

- {% badge text="New" type="success" /%} **Keyboard Shortcuts**: Added [keyboard shortcut](../keyboard-shortcuts.md) to scroll in index to active page.

### 19 Apr

- {% badge text="New" type="success" /%} **Theme**: Top navigation bar collapses with animation when on mobile layout.

### 18 Apr

- {% badge text="Improvement" /%} **API Reference**: On selecting a server URL, it will be remembered on next loads of the API reference.

### 17 Apr

- {% badge text="New" type="success" /%} **Version**: [Lock versions](../project-settings/managing-versions.md#locking-versions) to prevent further edits.

### 16 Apr

- {% badge text="New" type="success" /%} **API**: [GET - Search content](/v1.0/api/ref#search) can search in a specific section.

### 5 Apr

- {% badge text="Bug Fix" type="error" /%} **Page Info**: Go To button should be disabled when version or documentation is unpublished.

### 20 Mar

- {% badge text="New " type="success" /%} **404 Page**: A [landing page](../landing-page.md#404-page) can be designated as a 404 page.
- {% badge text="Update" type="warning" /%} **Icons**: Font Awesome is upgraded to latest v5 version.

### 18 Mar

- {% badge text="New" type="success" /%} **API**: [PUT - Publish API reference](/v1.0/api/ref#publish-reference) publishes an API reference.
- {% badge text="Change" type="warning" /%} **API**: [POST - Adds or updates a reference specification](/v1.0/api/ref#add-reference) takes a query `publish` which allows creating or updating an API reference in draft state.
- {% badge text="Change" type="warning" /%} **API Reference**: On creating an API reference, the initial contents would be in draft state, not a published state.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: When a version is cloned, the first edit history of an API reference was un-viewable.

### 15 Mar

- {% badge text="New" type="success" /%} **API Key**: Set up multiple API keys in a project.
- {% badge text="New" type="success" /%} **API Key**: API keys now have fine-permissions.
- {% badge text="New" type="success" /%} **Export**: We now have internal tools to move documentation to another project.

### 6 Mar

- {% badge text="Bug Fix" type="error" /%} **Index**: Move and rearrange poppers in editor were not showing at the correct place.

### 14 Feb

- {% badge text="Bug Fix" type="error" /%} **Glossary**: Search functionality for glossary terms was not working.

### 8 Feb

- {% badge text="Improvement" /%} **Top Navigation**: When the sections won't fit, an overlay scrollbar would show now.

### 7 Feb

- {% badge text="Bug Fix" type="error" /%} **API Reference**: Layout could have been wider than view port if an example has a very long title.

### 4 Feb

- {% badge text="New" type="success" /%} **Email Invite**: Customise [message that shows](../private-docs/email-invite.md#email-invite-customisation) when no such email invite exists.

### 15 Jan

- {% badge text="Bug Fix" type="error" /%} **Index**: Internal links were navigating to when clicked in the editor.

### 14 Jan

- {% badge text="New" type="success" /%} **SSO**: More SSO [configuration](../editor-single-sign-on--sso-.md#configuration) is available.

### 8 Jan

- {% badge text="New" type="success" /%} **Tags**: [Tag](../tags.md) pages to show [related pages](../tags.md#related-pages) and [search tag filtering](../tags.md#search-tag-filtering).
