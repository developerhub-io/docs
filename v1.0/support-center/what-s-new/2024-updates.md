---
type: page
title: 2024 Updates
listed: true
slug: 2024-updates
description: 
index_title: 2024 Updates
hidden: 
keywords: 
tags: 
---


See [Upcoming Features](/support-center/upcoming-features) to know what we're currently working on.

## 2024 Updates

### 24 Dec

- {% badge type="success" text="New " /%} **Code Steps:** Add [code walkthroughs](/support-center/code-steps) to your documentation.

### 23 Dec

- {% badge type="info" text="Improvement" /%} **Editor**: Major improvement for pasting content.

### 18 Dec

- {% badge type="success" text="New" /%} **Developer Tools**: `onreferencecontentloaded` [event](/support-center/developer-tools#on-reference-content-loaded) available to modify API reference UI as needed.
- {% badge type="info" text="Improvement" /%} **API Playground**: Bearer would be added automatically to the request with bearer security scheme.

### 17 Dec

- {% badge type="error" text="Bug Fix" /%} **Tables**: Fix to deleting first column on a new table and setting columns widths.

### 16 Dec

- {% badge type="info" text="Improvement" /%} **Editor**: Pasting improvements for variables, glossary and links.

### 13 Dec

- {% badge type="success" text="New" /%} **API Reference**: `x-enum-varnames` now supported as an [OpenAPI extension](/support-center/openapi-extensions).

### 5 Dec

- {% badge type="success" text="New" /%} **GitHub Sync**: [Sync your docs](/support-center/github-sync) with GitHub.

### 3 Dec

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Requests with `application/x-www-form-urlencoded` content type having special characters did not have them encoded.

### 28 Nov

- {% badge type="error" text="Bug Fix" /%} **API Playground**: Requests with `application/x-www-form-urlencoded` content type were handled as query string.

### 25 Nov

- {% badge type="success" text="New" /%} **Readability Metrics**: Right sidebar indicator for [readability](/support-center/readability-metrics) for English content.

### 13 Nov

- {% badge type="info" text="Improvement" /%} **API Reference**: Password OAuth2 flow type now accepts client authentication pair in the API playground.

### 11 Nov

- {% badge type="info" text="Improvement" /%} **API Reference**: Example requests and responses show summary in the select list instead of key.

### 25 Oct

- {% badge type="info" text="Improvement" /%} **Landing Page**: Variables written in default landing page layout would be rendered automatically.

### 24 Oct

- {% badge type="success" text="New" /%} **Landing Page**: Variables written in landing pages or custom pages would be rendered automatically.
- {% badge type="success" text="New" /%} **Custom Login**: `jti` parameter can be used to make a single JWT valid for only one device.
- {% badge type="info" text="Improvement" /%} **Feedback**: Further measures to block spam.
- {% badge type="info" text="Improvement" /%} **Feedback**: Can disable feedback using [advanced settings](/support-center/advanced-settings) according to [referrer](/support-center/feedback#feedback-spam-filter).

### 22 Oct

- {% badge type="error" text="Bug Fix" /%} **Import**: Fix to project imports where page headers might show.

### 13 Oct

- {% badge type="success" text="New" /%} **Editor**: [auto$](/support-center/blocks) and inline blocks can now be added by typing {% key key="/" /%} anywhere.
- {% badge type="info" text="Improvement" /%} **Editor**: Several improvements to blocks to make it easier to edit docs completely using keyboard without having to move the cursor, as well as cosmetic enhancements.
- {% badge type="info" text="Improvement" /%} **AI Features**: All our AI features use the enhanced `gpt-4o-mini` model now.

### 8 Oct

- {% badge type="error" text="Bug Fix" /%} **Feedback**: Feedback chart used to fail to load in rare cases.
- {% badge type="error" text="Bug Fix" /%} **Feedback**: Long and unusual feedback messages could've broken the dashboard layout.

### 27 Sep

- {% badge type="success" text="New" /%} **Video**: Start a youtube video at a certain time.

### 24 Sep

- {% badge type="info" text="Improvement" /%} **General**: Upgraded our databases to the latest and greatest.
- {% badge type="error" text="Bug Fix" /%} **Export**: Non-standard characters now become underscores in exported file names.
- {% badge type="error" text="Bug Fix" /%} **Comments**: User selector was not opening every time when hitting `@` in the comments box.

### 18 Sep

- {% badge type="info" text="Improvement" /%} **API Reference**: Recognise `date` string format.

### 17 Sep

- {% badge type="error" text="Bug Fix" /%} **Editor**: Page options were making page wider if the page slug was too long.

### 15 Sep

- {% badge type="success" text="New" /%} **API Reference**: Support for `x-tagGroups` for tag grouping.
- {% badge type="warning" text="Change" /%} **Editor**: Editor toolbar has a new look.

### 14 Sep

- {% badge type="info" text="Improvement" /%} **UI Translation**: Added `search.ai.answer`.

### 9 Sep

- {% badge type="success" text="New" /%} **API Reference**: Deprecated fields in response schemas are now shown in strikethough format.

### 7 Sep

- {% badge type="error" text="Bug Fix" /%} **Synced Block**: Importing a page that has invalid synced block IDs was failing the import.

### 2 Sep

- {% badge type="success" text="New" /%} **Tables**: Ability to reorder columns and rows.

### 31 Aug

- {% badge type="info" text="Improvement" /%} **Inlines Images**: Further improvement to resizing images.

### 30 Aug

- {% badge type="success" text="New" /%} **Inline Images**: Fit width mode available to take 100% of container space.
- {% badge type="info" text="Improvement" /%} **SEO**: XML sitemaps are made default.
- {% badge type="error" text="Bug Fix" /%} **Search**: Organisation search was down.

### 29 Aug

- {% badge type="success" text="New" /%} **Inline Images**: [auto$](/support-center/inline-images) are now available in beta. Great for tables!

### 28 Aug

- {% badge type="success" text="New" /%} **Code block**: [Highlighting lines](/support-center/code-blocks#highlight-code) is now available.
- {% badge type="success" text="New" /%} **Code block**: A local setting to [show line numbers](/support-center/code-blocks#show-line-numbers) is available.
- {% badge type="error" text="Bug Fix" /%} **Search**: Some headings were unreachable due to different fragment links.
- {% badge type="error" text="Bug Fix" /%} **AI Search**: Logs were not downloading fully in certain situations.

### 27 Aug

- {% badge type="info" text="Improvement" /%} **Email Invite**: [Two step magic link](/support-center/email-invite#troubleshooting) is available in case links are getting used by email security software.
- {% badge type="error" text="Bug Fix" /%} **Login**: A bug was introduced on 18 Aug which changed how we log in users. All users who have tried to log in since 18 Aug needed to reset their password. We have fixed that bug and old credentials are working again. Unfortunately, users who reset their passwords must change their passwords again.

### 26 Aug

- {% badge type="error" text="Bug Fix" /%} **Editor**: Instant markdown formatting was not showing in callouts.
- {% badge type="error" text="Bug Fix" /%} **Page Linking**: API reference operations were not showing if the API reference was not published yet.

### 22 Aug

- {% badge type="error" text="Bug Fix" /%} **SEO**: Sitemaps were erroring.

### 21 Aug

- {% badge type="error" text="Bug Fix" /%} **Email Invites**: Fixed error message when the invite is expired.

### 18 Aug

- {% badge type="info" text="Improvement" /%} **General**: We have huge infrastructure updates, we are all up to date!

### 14 Aug

- {% badge type="error" text="Bug Fix" /%} **Editor**: Pasting links in the links box did not have an effect.

### 13 Aug

- {% badge type="error" text="Bug Fix" /%} **Editor**: Pasting images inside list items was duplicating the image.

### 12 Aug

- {% badge type="error" text="Bug Fix" /%} **Editor**: Inline code formatting button on the toolbar was not working.

### 8 Aug

- {% badge type="success" text="New" /%} **Redirect**: Complete site redirects possible now by contacting us.

### 31 Jul

- {% badge type="warning" text="Change" /%} **API References**: Writers can [create and edit](/support-center/collaboration) API references in draft now.

### 24 Jul

- {% badge type="info" text="Improvement" /%} **AI Search**: Now using `gpt-4o-mini` model which provides more reasoning in the answers.

### 22 Jul

- {% badge type="info" text="Improvement" /%} **General**: We've had multiple performance improvements throughout the editor.
- {% badge type="error" text="Bug Fix" /%} **General**: Users in South Africa were unable to load the site due to an AWS failure.

### 18 Jul

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Jumping to heading on first load was some pixels out of view.

### 8 Jul

- {% badge type="warning" text="Change" /%} **SEO**: Sitemaps are now generated every 6 hours.

### 6 Jul

- {% badge type="warning" text="Change" /%} **Custom Login**: JWTs can only be signed using an API Key that has `access.write` permission.
- {% badge type="info" text="Improvement" /%} **General**: We've updated our front-end libraries completely. Using the latest technology now!

### 26 Jun

- {% badge type="error" text="Bug Fix" /%} **Editor**: Formatting text using toolbar as inline code was not activating save button.

### 25 Jun

- {% badge type="success" text="New" /%} **Table**: Ability to duplicate rows and columns.

### 24 Jun

- {% badge type="info" text="Improvement" /%} **Search**: Many improvements and bug fixes for [auto$](/support-center/ai-search).

### 23 Jun

- {% badge type="success" text="New" /%} **Page Linking**: Pages now have [permalinks](/support-center/page-linking#page-permalinks).

### 22 Jun

- {% badge type="success" text="New" /%} **Search**: [auto$](/support-center/ai-search) is now available for testing in beta for all grow and enterprise plans users.

### 5 Jun

- {% badge type="success" text="New" /%} **SSO**: Assign roles to users using attributes.
- {% badge type="info" text="Improvement" /%} **General**: User invites would default to the role set up for SSO, if set.

### 1 Jun

- {% badge type="error" text="Bug Fix" /%} **Github Code**: Markdown files were not styled correctly.

### 22 May

- {% badge type="success" text="New" /%} **Editors**: Grow plan projects can have more than 20 editors. See [pricing](https://developerhub.io/pricing).

### 18 May

- {% badge type="success" text="New" /%} **Search**: AI Search is now available in alpha.
- {% badge type="success" text="New" /%} **API**: [GET - Read reference](/v1.0/api/ref#read-reference) is now available.
- {% badge type="success" text="New" /%} **API**: [GET - Get all resources](/v1.0/api/ref#all-project) has two new query parameters `versionId` and `published`, and it provides `published` for all items.
- {% badge type="info" text="Improvement" /%} **API Reference**: Long response examples would be collapsed by default if possible.

### 14 May

- {% badge type="success" text="New " /%} **Find & Replace**: Find and Replace now supports searching in Custom HTML blocks.
- {% badge type="success" text="New" /%} **API Reference**: New setting to only show request payload without code samples.

### 24 Apr

- {% badge type="success" text="New" /%} **Feedback**: Feedback can be [marked as spam](/support-center/feedback#where-can-i-find-the-received-feedback).
- {% badge type="success" text="New" /%} **Feedback**: Spam messages can be [filtered automatically](/support-center/feedback#feedback-spam-filter).
- {% badge type="success" text="New" /%} **Feedback**: Personal identifiable information can be [redacted automatically](/support-center/feedback#redact-pii-from-feedback).

### 22 Apr

- {% badge type="success" text="New" /%} **Team**: Writers can now re-arrange pages in index.
- {% badge type="success" text="New" /%} **General**: We will notify you when you're using an out-dated version of our site.

### 20 Apr

- {% badge type="success" text="New" /%} **Keyboard Shortcuts**: Added [keyboard shortcut](/support-center/keyboard-shortcuts) to scroll in index to active page.

### 19 Apr

- {% badge type="success" text="New" /%} **Theme**: Top navigation bar collapses with animation when on mobile layout.

### 18 Apr

- {% badge type="info" text="Improvement" /%} **API Reference**: On selecting a server URL, it will be remembered on next loads of the API reference.

### 17 Apr

- {% badge type="success" text="New" /%} **Version**: [Lock versions](/support-center/managing-versions#locking-versions) to prevent further edits.

### 16 Apr

- {% badge type="success" text="New" /%} **API**: [GET - Search content](/v1.0/api/ref#search) can search in a specific section.

### 5 Apr

- {% badge type="error" text="Bug Fix" /%} **Page Info**: Go To button should be disabled when version or documentation is unpublished.

### 20 Mar

- {% badge type="success" text="New " /%} **404 Page**: A [landing page](/support-center/landing-page#404-page) can be designated as a 404 page.
- {% badge type="warning" text="Update" /%} **Icons**: Font Awesome is upgraded to latest v5 version.

### 18 Mar

- {% badge type="success" text="New" /%} **API**: [PUT - Publish API reference](/v1.0/api/ref#publish-reference) publishes an API reference.
- {% badge type="warning" text="Change" /%} **API**: [POST - Adds or updates a reference specification](/v1.0/api/ref#add-reference) takes a query `publish` which allows creating or updating an API reference in draft state.
- {% badge type="warning" text="Change" /%} **API Reference**: On creating an API reference, the initial contents would be in draft state, not a published state.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: When a version is cloned, the first edit history of an API reference was un-viewable.

### 15 Mar

- {% badge type="success" text="New" /%} **API Key**: Set up multiple API keys in a project.
- {% badge type="success" text="New" /%} **API Key**: API keys now have fine-permissions.
- {% badge type="success" text="New" /%} **Export**: We now have internal tools to move documentation to another project.

### 6 Mar

- {% badge type="error" text="Bug Fix" /%} **Index**: Move and rearrange poppers in editor were not showing at the correct place.

### 14 Feb

- {% badge type="error" text="Bug Fix" /%} **Glossary**: Search functionality for glossary terms was not working.

### 8 Feb

- {% badge type="info" text="Improvement" /%} **Top Navigation**: When the sections won't fit, an overlay scrollbar would show now.

### 7 Feb

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Layout could have been wider than view port if an example has a very long title.

### 4 Feb

- {% badge type="success" text="New" /%} **Email Invite**: Customise [message that shows](/support-center/email-invite#email-invite-customisation) when no such email invite exists.

### 15 Jan

- {% badge type="error" text="Bug Fix" /%} **Index**: Internal links were navigating to when clicked in the editor.

### 14 Jan

- {% badge type="success" text="New" /%} **SSO**: More SSO [configuration](/support-center/single-sign-on--sso-#configuration) is available.

### 8 Jan

- {% badge type="success" text="New" /%} **Tags**: [Tag](/support-center/tags) pages to show [related pages](/support-center/tags#related-pages) and [search tag filtering](/support-center/tags#search-tag-filtering).

