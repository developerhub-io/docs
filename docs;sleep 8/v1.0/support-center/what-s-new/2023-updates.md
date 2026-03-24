---
type: page
title: 2023 Updates
listed: true
slug: 2023-updates
description: 
index_title: 2023 Updates
hidden: 
keywords: 
tags: 
---

### 20 Dec

- {% badge type="error" text="Bug Fix" /%} **Index**: Categories were collapsible even though they are set not to.

### 19 Dec

- {% badge type="info" text="Improvement" /%} **Next UI**: If navigation bar has too many sections, it would collapse into a section picker (like the one on mobile). Only applies on non-Mac devices.

### 14 Dec

- {% badge type="success" text="New" /%} **Glossary**: Add [terms and definitions](/support-center/glossary) to your docs for contextual help.

### 11 Dec

A huge update to %product% UI.

- {% badge type="success" text="New" /%} **UI**: [Next UI](/support-center/customising-visuals#next-ui) is now available with sleek navigation bar, new search experience and clearer index.
- {% badge type="success" text="New" /%} **Customisation**: Ability to change [navigation link colours](/support-center/customising-visuals#changing-colours).
- {% badge type="success" text="New" /%} **Customisation**: Ability to make the [top navigation bar sticky](/support-center/customising-visuals#sticky-top-navigation-bar) to the top of the page.
- {% badge type="warning" text="Change" /%} **Documentation**: Minimal layout is no longer supported.
- {% badge type="warning" text="Change" /%} **Documentation**: Only scrollable indices are now supported.
- {% badge type="info" text="Improvement" /%} **UI**: Index is now placed to the side of the page, and content with TOC is in the middle.
- {% badge type="info" text="Improvement" /%} **Theme**: Theme toggle looks better.
- {% badge type="info" text="Improvement" /%} **UI**: Dropdowns look better and are animated when they show.

### 27 Nov

- {% badge type="error" text="Bug Fix" /%} **Project**: Deleting project that had PDF exports resulted in errors.

### 19 Nov

- {% badge type="success" text="New" /%} **Keywords**: Added [page keywords](/support-center/using-search#page-keywords) to improve search results.

### 18 Nov

- {% badge type="warning" text="Change" /%} **Plans**: All plans subscribed to before 2020 feature now 180 days of page history.

### 27 Oct

- {% badge type="info" text="Improvement" /%} **API References**: When no `operationId` is set and summaries are duplicated, the `operationId` we autogenerate would be suffixed by a counter so that the operations remain linkable. Setting own unique operationIds is still highly recommended.
- {% badge type="info" text="Improvement " /%} **API References**: Any response media type containing XML would have the example response syntax formatted to XML.

### 25 Oct

- {% badge type="success" text="New" /%} **SSO**: Ability to set up multiple SSO integrations with the same IdP.

### 18 Oct

- {% badge type="success" text="New " /%} **API Reference**: Enums of array items are now shown.

### 15 Oct

- {% badge type="error" text="Bug Fix" /%} **API Editor**: Saving existing API definitions showed "Uploaded file is not a text file" when the file was actually text.

### 12 Oct

- {% badge type="success" text="New " /%} **Advanced Settings**: Added option to control scroll offset which is useful when the top navigation bar is sticky.

### 5 Oct

- {% badge type="success" text="New" /%} **General**: Dark mode is now the default for all new projects.
- {% badge type="error" text="Bug Fix" /%} **Variables**: Query params added to load variables on public sites were not automatically removed.

### 20 Sep

- {% badge type="error" text="Bug Fix" /%} **Feedback**: Fixed an issue where project feedback was failing to show at times.

### 15 Sep

- {% badge type="error" text="Security" /%} **Update:** Our whole stack has been updated for better security.

### 2 Sep

- {% badge type="info" text="Improvement" /%} **Slack**: Updates are now sent directly rather than every 15 minutes.

### 28 Aug

- {% badge type="success" text="New" /%} **Code Blocks**: Add [setting](/support-center/advanced-settings) to show line numbers in the gutter.

### 26 Aug

- {% badge type="error" text="Bug Fix" /%} **Cloning**: Pages having duplicate slugs would have duplicate content when their versions are cloned.

### 23 Aug

- {% badge type="success" text="New" /%} **Export**: Projects can be exported in markdown format. Applies to [GET - Exports project](/v1.0/api/ref#export-project) as well.

### 18 Aug

- {% badge type="error" text="Bug Fix" /%} **Images**: Writers were unable to upload images.

### 13 Aug

- {% badge type="success" text="New" /%} **Intercom**: Add a %product% search widget to your messenger home.

### 11 Aug

- {% badge type="success" text="New" /%} **Enterprise**: Organisation owners can track usage and see SSO status from the sidebar &gt; Organisation {% icon classes="fas fa-building" /%}.

### 10 Aug

- {% badge type="info" text="Improvement" /%} **AI Summarisation**: Longer pages can now also be summarised.

### 7 Aug

- {% badge type="success" text="New" /%} **AI Summarisation**: Use [auto$](/support-center/ai-summarisation) to generate META descriptions of pages.

### 5 Aug

- {% badge type="error" text="Bug Fix" /%} **General**: Fix to all input modals where their functionality could have been triggered multiple times.

### 26 Jul

- {% badge type="success" text="New" /%} **Landing Pages**: Adding [other landing pages](/support-center/landing-page) at a non-root path is now available.

### 13 Jul

- {% badge type="error" text="Bug Fix" /%} **API References**: URLs with fragment did not scroll if tags were set to be expandable.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Better handling of accents in page titles when creating a page.

### 6 Jul

- {% badge type="success" text="New" /%} **Theme**: Dark [theme](/support-center/theme) is now available.
- {% badge type="success" text="New" /%} **Developer Tools**: New [Navigate to Path](/support-center/developer-tools#navigate-to-path) function.
- {% badge type="warning" text="Change" /%} **Developer Tools**: [Navigate to URL (Deprecated)](/support-center/developer-tools#navigate-to-url-deprecated) is now deprecated.
- {% badge type="info" text="Improvement" /%} **CSS**: New [CSS Variables](/support-center/custom-css#css-variables) for easier customisation.
- {% badge type="error" text="Bug Fix" /%} **Stability**: Various bug fixes around stability.

### 1 Jul

- {% badge type="error" text="Bug Fix" /%} **Tables**: Hitting {% key key="Tab" /%} was causing infinite rows when on the last column of the table heading.

### 21 Jun

- {% badge type="success" text="New " /%} **Table of Contents**: Highlights last scrolled to heading by default. Can be disabled from [advanced settings](/support-center/advanced-settings).
- {% badge type="success" text="New" /%} **Table of Contents**: H4 now shows in TOC. Can be disabled from [advanced settings](/support-center/advanced-settings).
- {% badge type="success" text="New" /%} **Images**: Images now lazy-load to gain faster page loads.

### 18 Jun

Today we bring a large overhaul of %product%'s codebase after months of work to be able to build features quicker and better. The new codebase is simpler, 10% smaller, and faster.

- {% badge type="success" text="New" /%} **Broken Links**: Duplicate slugs are reported when analysing broken links.
- {% badge type="success" text="New" /%} **Editor**: Added a page refresh button under the page title. Clicking on the page in the index would not refresh it anymore.
- {% badge type="success" text="New" /%} **Developer Tools**: Added `goHome()` function to navigate home.
- {% badge type="warning" text="Change" /%} **Page Info**: Duplicate slugs are no longer allowed. If a page, section or version has a duplicate slug, then you'll be forced to modify it to make it accessible.
- {% badge type="warning" text="Change" /%} **Embed**: Using `?goto=embed` is no longer supported. Use `?mode=embed` instead.
- {% badge type="info" text="Improvement" /%} **Navigation**: Handles faster user navigation better when page has not loaded yet.
- {% badge type="info" text="Improvement" /%} **URL Strategy**: Modified [URL Strategy](/support-center/previewing-documentation#url-strategy). `/ref` has been dropped from API Reference URLs, and dash URLs have been deprecated (`/-/-/-`).
- {% badge type="info" text="Improvement" /%} **Navigation**: Browser back button functionality improved for both editor and reader modes.
- {% badge type="info" text="Improvement" /%} **Landing Page**: Using `openLink` is no longer needed to navigate internally. Added a [new function](/support-center/developer-tools#make-all-landing-page-links-route-in-spa) to use for dynamically generated anchors.
- {% badge type="info" text="Improvement" /%} **Performance**: Smoother UI interactions.
- {% badge type="info" text="Improvement" /%} **Editor**: Links all around the editor are openable in a new tab (in dashboard, feedback, comments...)
- {% badge type="error" text="Bug Fix" /%} **Index**: Parent pages that have all child pages hidden from index were showing the chevron icon.
- {% badge type="error" text="Bug Fix" /%} **Index**: Duplicating a hidden index was not setting it as hidden.

### 16 Jun

- {% badge type="error" text="Bug Fix" /%} **Export**: Large projects had intermittent issues getting exported.

### 8 Jun

- {% badge type="success" text="New" /%} **SEO**: Sitemaps in XML format are now available at `/sitemap.xml` under the basepath of the docs site.

### 23 May

- {% badge type="success" text="New" /%} **Developer Tools**: Added ability to [zoom images](/support-center/developer-tools#zoom-image) using javascript for dynamically generated images.

### 16 May

- {% badge type="success" text="New" /%} **Developer Tools**: Added `onfeedback` event.
- {% badge type="success" text="New" /%} **Integrations**: Added instructions for embedding [PlantUML](/support-center/graphs-charts#plantuml).

### 11 May

- {% badge type="success" text="New" /%} **SEO**: Add description for landing page.

### 3 May

- {% badge type="success" text="New" /%} **Developer Tools**: Added [Get Active Version](/support-center/developer-tools#get-active-version), [Get Active Section](/support-center/developer-tools#get-active-section) and [Get Active Page](/support-center/developer-tools#get-active-page) functions.

### 27 Apr

- {% badge type="info" text="Improvement" /%} **API Reference**: Add support for `application/x-www-form-urlencoded` for OpenAPI 3 definitions in [auto$](/support-center/try-it-out).

### 26 Apr

- {% badge type="info" text="Improvement" /%} **API Reference**: Show the first example for query strings if only `examples` is provided in OpenAPI definition.

### 17 Apr

- {% badge type="info" text="Improvement" /%} **API Reference**: Further support for oneOf/anyOf in response bodies.
- {% badge type="info" text="Improvement" /%} **API Reference**: Further support for oneOf/anyOf in autogenerated examples.
- {% badge type="info" text="Improvement" /%} **Quick Switcher**: Results can be opened in a new tab.
- {% badge type="error" text="Bug Fix" /%} **Notifications**: Oops we made notifications too short. Fixed now.

### 12 Apr

- {% badge type="success" text="New" /%} **Quick Switcher**: [auto$](/support-center/quick-switcher) can now find text in the page, and perform find & replace inside the editor.

### 29 Mar

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Examples with value 0 were showing the placeholder.
- {% badge type="error" text="Bug Fix" /%} **UI Translation**: Changing between different sections with different languages was not changing the UI translations.

### 28 Mar

- {% badge type="info" text="Improvement" /%} **SEO**: Generated page description are now as long as possible, under 200 characters.

### 24 Mar

- {% badge type="success" text="New" /%} **Search**: Added a [javascript event](/support-center/developer-tools#on-search) for when a search operation happens.
- {% badge type="info" text="Improvement" /%} **Custom HTML**: Headings in custom HTML blocks now show in the table of contents.

### 23 Mar

- {% badge type="success" text="New" /%} **SEO**: Added a setting to [canonicalize short URL form](/support-center/seo) directly from Project Settings.

### 20 Mar

- {% badge type="info" text="Improvement" /%} **Search**: By default, stop words are removed now.

### 17 Mar

- {% badge type="error" text="Bug Fix" /%} **Head Tags**: Scripts with special attributes did not have the attributes added correctly.

### 5 Mar

- {% badge type="success" text="New" /%} **SEO**: Page titles can be formatted to include more than page title and project title using [advanced settings](/support-center/advanced-settings).

### 2 Mar

- {% badge type="success" text="New" /%} **APIs**: [Read page](/v1.0/api/ref#read-page) can provide the content in HTML format.
- {% badge type="info" text="Improvement" /%} **SEO**: Improvement to META description for pages starting with non-text content.
- {% badge type="info" text="Improvement" /%} **SEO**: We added support for SEO software suits to be able to analyse your project sites without any configuration change.
- {% badge type="info" text="Improvement" /%} **SEO**: Our pages now rank at 100% in Google's Lighthouse SEO test.

### 21 Feb

- {% badge type="info" text="Improvement" /%} **Private Docs**: Prevent infinite page reloading if the URL does not include the basepath of the project.

### 15 Feb

- {% badge type="error" text="Bug Fix" /%} **Shared Link**: Shared links did not include the project basepath.

### 14 Feb

- {% badge type="error" text="Bug Fix" /%} **Dashboard**: Fixed analytics layout when search terms are too large.

### 19 Jan

- {% badge type="success" text="New " /%} **APIs**: [Get all resources](/v1.0/api/ref#all-project) provides slugs of pages, API references, documentation, and versions.
- {% badge type="success" text="New" /%} **APIs**: [Read page](/v1.0/api/ref#read-page) can provide the content in markdown format. It also adds page paths.

### 4 Jan

- {% badge type="info" text="Improvement" /%} **API Playground**: Added better handling for APIs that return errors and the messages that show.
- {% badge type="error" text="Bug Fix" /%} **Tabs**: Dots in tab titles were breaking tab navigation.
- {% badge type="error" text="Bug Fix" /%} **General**: Fixed a bunch of general error messages that were showing due to rate limiting.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Server selector was not showing for OpenAPI 2 definitions.

### 2 Jan

- {% badge type="success" text="New" /%} **Import**: [Zendesk migration](/support-center/import-from-zendesk) to %product% tool is available now.