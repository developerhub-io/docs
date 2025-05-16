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

### 16 May

- {% badge type="success" text="New" /%} **Top Navigation Bar**: [Navigation groups](/support-center/top-navigation-bar#navigation-structure) can be created to group documentation sections and API references in the top navigation bar.
- {% badge type="success" text="New" /%} **API References**: `--required-text` CSS variable available to change the text showing up when a field is required, defaults to `*`.
- {% badge type="info" text="Improvement" /%} **Index**: Index scroll functional regardless of custom customisations made to the top navigation.
- {% badge type="info" text="Improvement" /%} **General**: Deprecated `scrolling` [advanced setting](/support-center/advanced-settings). Scrolling offsets would be calculated automatically.
- {% badge type="warning" text="Change" /%} **Callouts**: Callouts no longer use table HTML markup. They use flexbox instead for easier customisation.
- {% badge type="error" text="Bug Fix" /%} **Landing Page**: Landing page in edit mode was showing up stacked when changed.

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