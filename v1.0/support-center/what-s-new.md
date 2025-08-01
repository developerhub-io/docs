---
type: page
title: What's New (2025)
listed: true
slug: what-s-new
description: 
index_title: What's New (2025)
hidden: 
keywords: release notes
tags: 
---

See [Upcoming Features](/support-center/upcoming-features) to know what we're currently working on.

## 2025 Updates

### 28 Jul

- {% badge type="success" text="New" /%} **Index**: Index can be as hierarchical as needed. Pages can grand-grand-grand father other pages. Also, the index is now MUCH faster 🚀
- {% badge type="warning" text="CSS Changes" /%} **Index**: Index chevron icon is moved to the right and the margins are changed. We've pinned the frontend deployment application for some projects to DeveloperHub version from 24th of July 2025.

### 17 Jul

- {% badge type="success" text="New" /%} **Labels**: New index item ["Label"](/support-center/categories#labels) to add text and group page.
- {% badge type="error" text="Bug Fix" /%} **Import**: Multiple bug fixes to importing projects.

### 16 Jul

- {% badge type="info" text="Improvement" /%} **Cards**: Further improvements to usability and keyboard shortcuts.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Better handling when backspace is pressed at start of a list.

### 15 Jul

- {% badge type="success" text="New" /%} **Cards**: [auto$](/support-center/cards) block available to highlight and link to main pages.

{% cards view="grid" %}
{% card title="Getting Start" link="/support-center/getting-started" %}
This goes to the start
{% /card %}
{% card title="Cards" link="/support-center/cards" %}
See the docs about cards
{% /card %}
{% /cards %}

### 10 Jul

- {% badge type="success" text="New" /%} **Code Block**: Lines wrap automatically when a line exceeds 120 characters. Added an option to disable or enable line wrapping per code block.

### 7 Jul

- {% badge type="success" text="New" /%} **API Key**: API keys can be cloned and renewed.
- {% badge type="info" text="Improvement" /%} **LLMs**: API references have a `.md` page.

### 1 Jul

- {% badge type="success" text="New" /%} **LLMs**: `llms.txt` is now [supported](/support-center/llms-txt).

### 30 Jun

- {% badge type="info" text="Improvement" /%} **GitHub Sync**: Creating files in GitHub creates published pages on DeveloperHub.

### 27 Jun

- {% badge type="success" text="New" /%} **API Key**: Revoked keys are now shown in the list, along with creation dates for all keys.
- {% badge type="error" text="Bug Fix" /%} **GitHub Sync**: Multiple fixes to sync process.

### 26 Jun

- {% badge type="error" text="Bug Fix" /%} **Editor**: Documentation sections ordering was not working.

### 25 Jun

- {% badge type="info" text="Improvement" /%} **Export API**: The [GET - Exports project](/v1.0/api/ref#export-project) API now supports exporting a specific version.
- {% badge type="error" text="Bug Fix" /%} **Export**: Exporting large projects was failing due to a timeout.
- {% badge type="error" text="Bug Fix" /%} **GitHub Sync**: Tables with assigned column widths caused syncing problems.

### 24 Jun

- {% badge type="success" text="New" /%} **Documentation**: Ability to copy documentation section to another version. 

### 23 Jun

- {% badge type="error" text="Bug Fix" /%} **Top Navigation**: Landing page button was not showing on mobile layout.

### 4 Jun

- {% badge type="success" text="New" /%} **Search**: Ability to [hide AI search](/support-center/advanced-settings) but keep the vector search available through API.
- {% badge type="error" text="Bug Fix" /%} **Top Navigation**: Top navigation was not scrollable when it had too many items.

### 3 Jun

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Fixed an issue where empty objects in example request/responses show as empty arrays.

### 28 May

- {% badge type="success" text="New" /%} **Enterprise Search**: Ability to search in certain version and section for [column search](/support-center/enterprise-search#column-search).

### 21 May

- {% badge type="info" text="Improvement" /%} **Synced Blocks**: Headings inside synced blocks are now shown in the table of contents when editing.

### 20 May

- {% badge type="success" text="New" /%} **Reader SSO**: [Single-Sign On (SSO)](/support-center/reader-single-sign-on) is now available for readers at the enterprise plan.

### 19 May

- {% badge type="success" text="New" /%} **Performance**: Enterprise only - switching pages just got blazing fast with preloaded pages 🚀
- {% badge type="error" text="Bug Fix" /%} **Editor**: Double underscores inside inline code inside callouts were transforming text into italics.

### 18 May

- {% badge type="success" text="New" /%} **CSS**: Ability to change the dropdown animation with `--dropdown-animation` [CSS variable](/support-center/custom-css#css-variables).
- {% badge type="info" text="Improvement" /%} **API Reference**: anyOf/oneOf now supported for inline schemas.
- {% badge type="info" text="Improvement" /%} **Import**: Pages that are not ordered correctly will no longer fail import.
- {% badge type="info" text="Improvement" /%} **Editor**: Using select all keyboard shortcuts inside blocks selects only text inside the block.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Highlighting endpoint during scrolling was not working for all endpoints.

### 16 May

- {% badge type="success" text="New" /%} **Top Navigation Bar**: [Navigation groups](/support-center/top-navigation-bar#navigation-structure) can be created to group documentation sections and API references in the top navigation bar.
- {% badge type="success" text="New" /%} **API References**: `--required-text` CSS variable available to change the text showing up when a field is required, defaults to `*`.
- {% badge type="info" text="Improvement" /%} **Index**: Index scroll functional regardless of custom customisations made to the top navigation.
- {% badge type="info" text="Improvement" /%} **General**: Deprecated `scrolling` [advanced setting](/support-center/advanced-settings). Scrolling offsets would be calculated automatically.
- {% badge type="warning" text="Change" /%} **Callouts**: Callouts no longer use table HTML markup. They use flexbox instead for easier customisation.
- {% badge type="error" text="Bug Fix" /%} **Landing Page**: Landing page in edit mode was showing up stacked when changed.

{% video videoId="https://uploads.developerhub.io/prod/02/nrz4mx3xlcly8g3w4amahs5n7a68nudf2ln5h4jaibjnilq6qhu89y3zseojqeu3.mp4?controls=0&autoplay=1&loop=1&muted=1&playsinline=1" provider="raw" %}
{% /video %}

### 14 May

- {% badge type="success" text="New" /%} **API Reference**: Now you can use markdown in response description.

### 4 May

- {% badge type="error" text="Bug Fix" /%} **Readability Metrics**: Icon UI was inconsistent when the page was being edited.
- {% badge type="error" text="Bug Fix" /%} **GitHub Sync**: Long pages with many blocks were not always deserialised correctly.
- {% badge type="info" text="Improvement" /%} **GitHub Sync**: Sync will not fail anymore if an image link is inaccessible. The image will remain broken on the page.

### 30 Apr

- {% badge type="error" text="Bug Fix" /%} **Versions**: Resolved an issue that could have caused the versions order to become out of sync.

### 26 Apr

- {% badge type="success" text="New" /%} **Developer Tools**: New javascript event [On Version Change](/support-center/developer-tools#on-version-change) and new functions [Get Active Project](/support-center/developer-tools#get-active-project) and [Get Active Version](/support-center/developer-tools#get-active-version). Index can now be retrieved using [Get Active Section](/support-center/developer-tools#get-active-section).
- {% badge type="info" text="Improvement" /%} **CSS Changes**: Many CSS and layout changes aiming at cleaning and simplifying code. Changes include:
    - Addition of `--font-size`, `--secondary-font-size`, `--index-width` and `--reference-index-width` variable additions.
    - Revamp of search container and results.
    - Preventing over-scroll for indices.
    - Fix to highlighted code colour.
    - Fix to code steps when top navigation is sticky.

- {% badge type="error" text="Bug Fix" /%} **Callouts**: Pasting inside callouts was not working under certain conditions.

### 9 Apr

- {% badge type="success" text="New" /%} **Editor**: First number of an item in an ordered list can be changed by right-clicking on it.

### 7 Apr

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Example responses selector was not showing.

### 31 Mar

- {% badge type="success" text="New" /%} **Theme**: [Light-themed code](/support-center/code-theme) blocks.
- {% badge type="success" text="New" /%} **API Reference**: The API references have been given a fresh new look! Exciting new features include:
    - An intuitive pop-out playground designed to enhance user interaction.
    - Dynamic endpoint highlighting in the index to facilitate smoother navigation.
    - A streamlined colour palette that contributes to a more aesthetically pleasing appearance.
    - Improved handling of word-breaking in tables to ensure better readability.
    - More straightforward response selection for user convenience.

{% video videoId="https://uploads.developerhub.io/prod/02/alfw0asaqyh1rzb2dnud9xzobfsc2l255qvbqq2pd97nrgz3pkd22pe6thc23xwm.mp4?controls=0&autoplay=1&loop=1&muted=1&playsinline=1" provider="raw" %}
{% /video %}

### 25 Mar

- {% badge type="error" text="Bug Fix" /%} **Editor**: Copy pasting list items could have caused errors while saving in some situations.

### 22 Mar

- {% badge type="info" text="Improvement" /%} **API Reference**: Code is not line wrapped by default anymore. Use `apiReference.lineWrapCode` [setting](/support-center/advanced-settings) to enable line wrapping.
- {% badge type="warning" text="Change" /%} **API Reference**: Changed GET `curl` requests syntax format.
- {% badge type="warning" text="Change" /%} **API Reference**: Rewrote the layout CSS. We no longer use bootstrap for API reference general layout.

### 20 Mar

- {% badge type="success" text="New" /%} **API Reference**: New setting to disable [auto-capitalizing tags](/support-center/api-reference-settings#auto-capitalize-tags).

### 18 Mar

- {% badge type="info" text="Improvement" /%} **Search Analytics**: Multiple improvements to click analytics charts.

### 14 Mar

- {% badge type="success" text="New" /%} **Search Analytics**: Clicks analytics is now also available for [enterprise search](/support-center/enterprise-search).

### 13 Mar

- {% badge type="success" text="New" /%} **Search Analytics**: We're now collecting analytics on clicks in searches.
- {% badge type="success" text="New" /%} **Search Analytics**: Click analytics are now available in [dashboard](/support-center/search-analytics). Data will be incomplete until 13 Apr 2025.

### 12 Mar

- {% badge type="success" text="New" /%} **Video**: [auto$](/support-center/videos) can now be uploaded too up to 10MB.
- {% badge type="info" text="Improvement" /%} **Editor**: Many blocks had their looks in edit mode updated.
- {% badge type="info" text="Improvement" /%} **Images**: Images can now be freely resized, removing image modes.

### 9 Mar

- {% badge type="success" text="New" /%} **AI Writer**: Type better, summarise, shorten, expand, enhance and more with [auto$](/support-center/ai-writer).
- {% badge type="success" text="New" /%} **AI Commit Messages**: Automatically annotate page history with [auto$](/support-center/ai-commit-messages).
- {% badge type="error" text="Bug Fix" /%} **Images**: Replace button was not functioning.

### 6 Mar

- {% badge type="error" text="Bug Fix" /%} **Comments**: Comment button in documentation toolbar was not opening the comments bar.
- {% badge type="error" text="Bug Fix" /%} **Code Steps**: Extra border was showing for code steps in the editor.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Selecting a block using keyboard right after a heading was formatting the heading to paragraph.

### 1 Mar

- {% badge type="info" text="Improvement" /%} **Server Headers**: Better support for [content security policy](/support-center/server-headers#content-security-policy) set up using server headers.

### 26 Feb

- {% badge type="success" text="New" /%} **PDF Export**: Ability to modify front and back page covers from the UI.
- {% badge type="success" text="New" /%} **PDF Export**: Can use multiple back page covers now to add multiple PDFs to the docs PDF.

### 20 Feb

- {% badge type="success" text="New" /%} **API**: New API to [lists all documentation section under a version](/v1.0/api/ref#list-documentation).
- {% badge type="success" text="New" /%} **Custom HTML**: [auto$](/support-center/custom-html) block now supports [variables](/support-center/variables).

### 19 Feb

- {% badge type="error" text="Bug Fix" /%} **Editor**: Dropdowns had a very dark border in light mode.
- {% badge type="error" text="Bug Fix" /%} **Index**: Long connected page titles now break instead of getting hidden.

### 27 Jan

- {% badge type="success" text="New" /%} **PDF Export**: PDF export jobs can be removed from the list.

### 22 Jan

- {% badge type="info" text="Improvement" /%} **Callout**: Modernised callout looks by increasing border radius and removing shadow.

### 20 Jan

- {% badge type="success" text="New" /%} **Comments**: [Comments](/support-center/comments#comments-in-api-references) are now available on API references where a specific part of the API reference can be tagged.

### 19 Jan

- {% badge type="info" text="Improvement" /%} **Editor**: Major improvements to copy & paste behaviour. Copying and pasting DeveloperHub content always has content ordered correctly now. Select All performs as expected.
- {% badge type="warning" text="Change" /%} **Editor**: In edit mode, we no longer show a dotted box around the selected content, instead a line shows on the left side.

### 12 Jan

- {% badge type="success" text="New" /%} **PDF Export**: Both public and private projects can now be exported.

### 3 Jan

- {% badge type="success" text="New" /%} **API Reference**: Extra [variables](/support-center/openapi-extensions#variables) available in API references.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Fix to navigating to anchor from markdown links when tags are expandable.