---
type: page
title: 2020 Updates
listed: true
slug: 2020-updates
description: 
index_title: 2020 Updates
hidden: 
keywords: 
tags: 
---


### 26 Dec

- {% badge type="success" text="New" /%} **API Reference**: Browsers can now cache the API Reference instead of requesting it every time from our servers.

### 25 Dec

- {% badge type="success" text="New" /%} **API Reference**: Added an option to [show content type](/support-center/api-reference-settings#show-content-type-header) header for requests with body.
- {% badge type="warning" text="Improvement" /%} **Raw HTML**: On saving/importing a page that has raw HTML, we now provide a verbose message which lets you know the first occurrence of raw HTML that prevented the operation.

### 24 Dec

- {% badge type="success" text="New" /%} **Dashboard**: You can now access a dashboard which provides you with latest comments and drafts pages so you can know where to start your day.
- {% badge type="success" text="New" /%} **OpenAPI3**: OpenAPI3 support is no longer in Beta 🎉
- {% badge type="success" text="New" /%} **API Reference**: Loading state now appears when switching to an API Reference for your readers.
- {% badge type="success" text="New" /%} **More Keyboard Shortcuts**: More [keyboard shortcuts](/support-center/keyboard-shortcuts) available to navigate through DeveloperHub.
- {% badge type="warning" text="Improvement" /%} **Quick Switcher**: Quick Switcher now looks through everything, not just the documentation you're on now.
- {% badge type="warning" text="Improvement" /%} **Quick Switcher**: You can now navigate using keyboard keys between search results.
- {% badge type="warning" text="Change" /%} **DOM & CSS**: Many changes to DOM and CSS changes have been made to allow us to build new features. Please review your project to ensure sustained compatibility.

### 16 Dec

- {% badge type="warning" text="Improvement" /%} **Performance**: Projects with multiple versions would load magnitudes faster now.

### 9 Dec

- {% badge type="error" text="Bug Fix" /%} **Export**: Exporting a documentation having the same page title for multiple parent pages used to merge pages in one folder.

### 8 Dec

- {% badge type="error" text="Bug Fix" /%} **Overlapping Items**: Search items used to overlap with code block lines due to incorrect z-index.
- {% badge type="error" text="Bug Fix" /%} **Go to top**: Clicking on a link for landing page did not use to scroll to top.

### 7 Dec

- {% badge type="warning" text="Improvement" /%} **Import/Export**: On export we ensure that all filenames have different titles so imports would not fail due to duplicate titles.

### 2 Dec

- {% badge type="success" text="New" /%} **Search through API**: We added a [search](/api/ref#search) to let you search your documentation from your website.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Schemas of type array did not show type correctly.

### 28 Nov

- {% badge type="warning" text="Change" /%} **Max upload size**: Max upload size is now capped at 20MB.
- {% badge type="warning" text="Change" /%} **Max page size**: Max page size on upload is 2MB. Enough to have all the words in Oxford dictionary.
- {% badge type="warning" text="Improvement" /%} **Page drag & drop**: Index autoscrolls when dragging a page and dropping it somewhere far in the index.
- {% badge type="error" text="Bug Fix" /%} **Custom event**: `onsectionchange` did not work as expected after category drag/drop changes on 1 Oct.
- {% badge type="success" text="New" /%} **Custom Javascript**: On changing [custom javascript](/support-center/custom-javascript), we will validate your script automatically and warn you if it is syntactically incorrect.

### 24 Nov

- {% badge type="error" text="Bug Fix" /%} **Duplicate Blocks**: Duplicating a code block and changing its content would change content for both blocks.

### 21 Nov

- {% badge type="success" text="New" /%} **Search Scope**: Modify search bar scope to search through only active documentation or reference using [advanced settings](/support-center/advanced-settings).
- {% badge type="warning" text="Improvement" /%} **Variables in Search**: [Variables](/support-center/variables) are now resolved when searching.

### 17 Nov

- {% badge type="error" text="Bug Fix" /%} **Page Import**: Page import used to break reverting to older history.
- {% badge type="success" text="New" /%} **Specific CSS Classes**: Specific classes are now also available for links in the index to help with customising CSS.
- {% badge type="error" text="Bug Fix" /%} **Page Ordering**: Page ordering could fail after a page was inserted under a category.

### 16 Nov

- {% badge type="success" text="New" /%} {% badge type="warning" text="Beta" /%} **See who's editing**: See which teammates are viewing the page you are on and who is editing it right below the Activity tab.

### 14 Nov

- {% badge type="error" text="Bug Fix" /%} **Page Saving**: Pages could not be saved for the first time when their title had a dot in it.

### 9 Nov

- {% badge type="success" text="New" /%} **Category Pages**: Create new pages under category directly by pressing the {% icon classes="fas fa-plus" /%} next to the category title.
- {% badge type="success" text="New" /%} **Manual Category Toggling:** Ability to allow manual toggling of categories when they are collapsible.

### 5 Nov

- {% badge type="info" text="Improvement" /%} **API References**: Updated our third party tools of validation API specs, increasing success rate.
- {% badge type="info" text="Improvement" /%} **API References**: Circular references are now handled by providing the object type.
- {% badge type="error" text="Bug Fix" /%} **Export**: Project export was broken when a project contains a separator in a documentation index.

### 25 Oct

- {% badge type="success" text="New" /%} **Separator**: Add [separators](/support-center/categories#separators) to the index.
- {% badge type="info" text="Improvement" /%} **Index Page Link**: [Link](/support-center/external-links) to other parts of your documentation in the index to open the links in the same tab.
- {% badge type="success" text="New" /%} **Mobile Index**: Mobile index has been redesigned to match the full index experience instead of a minimal dropdown.
- {% badge type="success" text="New" /%} **Specific CSS Classes**: Added specific classes for each index item based on the slug and internal ID. This is to help with [hiding pages](/support-center/unlisting-old#hiding-page) for example.

### 10 Oct

- {% badge type="error" text="Bug Fix" /%} **User roles**: Admins were not able to change other user roles from Team sidebar.
- {% badge type="error" text="Bug Fix" /%} **Landing page**: Landing page was not rendered for a few customers where they had links after categories.

### 1 Oct

- {% badge type="success" text="New" /%} **Expandable Categories**: Set categories [to collapse](/support-center/documentation-settings#collapsible-categories) by default.
- {% badge type="info" text="Improvement" /%} **Categories drag & drop**: Categories now carry the pages with them when dragged and dropped.

### 3 Sep

- {% badge type="success" text="New" /%} **Analyse links**: [Analyse](/support-center/page-linking) all links inside a version in one-go.
- {% badge type="success" text="New" /%} **Notify Breaking Links:** We'll notify you of all page links that will break when deleting a page.

### 30 Aug

- {% badge type="success" text="New" /%} **User roles**: Teammates can have different [roles](/support-center/collaboration#user-roles).

### 28 Aug

- {% badge type="info" text="Improvement" /%} **Images**: Images now retain highest quality on upload.

### 19 Aug

- {% badge type="error" text="Bug Fix" /%} **Cloning Version**: Cloning versions having OpenAPI 3 references was broken.

### 12 Aug

- {% badge type="success" text="New" /%} **UI Translation**: Change [UI text](/support-center/ui-translation) for each individual documentation directly from Documentation Settings.

### 11 Aug

- {% badge type="error" text="Bug Fix" /%} **Import**: Importing files containing numbers in their file name could have aborted import.
- {% badge type="error" text="Bug Fix" /%} **Import**: Importing files having blocks followed by a separator fails to show the block.
- {% badge type="info" text="Improvement" /%} **Empty Documentation**: Documentation with no published pages no longer shows in documentation list.
- {% badge type="error" text="Bug Fix" /%} **Code Blocks**: Pressing space while changing a code block title used to close the settings.

### 9 Aug

- {% badge type="info" text="Improvement" /%} **GA Tracking**: Google Analytics tracking for custom landing page to content links.

### 4 Aug

- {% badge type="success" text="New" /%} **OneOf/AnyOf Support**: OneOf/AnyOf keywords are now supported for requests and responses when used in top-level of schema.

### 1 Aug

- {% badge type="info" text="Improvement" /%} **Faster Page Load**: For your readers, pages get cached on the client-side, eliminating network request to read pages again.

### 26 Jul

- {% badge type="error" text="Bug Fix" /%} **References - Requests:** Requests code generation incomplete when switching between API references.
- {% badge type="info" text="Improvement" /%} **References - Performance**: Faster rendering of references.

### 6 Jul

- {% badge type="info" text="Improvement" /%} **Collapsible Code Block**: Code blocks having more than 100 lines have collapsible content automatically.
- {% badge type="warning" text="Change" /%} **Privacy Policy**: We have modified our [Privacy Policy](https://developerhub.io/privacy) to include our new address.

### 30 Jun

- {% badge type="success" text="New" /%} **Index Access**: Provide access to the index of a documentation when `onsectionchange` custom event is dispatched.
- {% badge type="warning" text="Change" /%} **Customise Class CSS**: Added a second class to `.customise` which identifies the section type `documentation` , `references` or `landing-page`.

### 24 Jun

- {% badge type="success" text="New" /%} **OpenAPI 3**: OpenAPI 3 beta support is available.

### 21 Jun

- {% badge type="success" text="New" /%} **Local Image Imports**: Images in an `assets` local folder can be imported in the %product% import ZIP file.
- {% badge type="info" text="Improvement" /%} **Imports**: %product% imports can be unordered.

### 16 Jun

- {% badge type="success" text="New" /%} **Allow Reference Download**: Introduced option to allow API References to be downloaded publicly.

### 10 Jun

- {% badge type="success" text="New" /%} **Inline Block in Headings**: Added support for inline blocks in headings.
- {% badge type="error" text="Bug Fix" /%} **Page Selector Updating**: Page selector did not update sometimes previously when new pages are added in the same session.

### 6 Jun

- {% badge type="error" text="Bug Fix" /%} **Page Heading Slugs:** When linking between pages, headings with symbols were generating slugs incorrectly.
- {% badge type="info" text="Improvement" /%} **Page Loading Position:** When jumping to a heading after a page load, now it positions better to the heading top if the page has lots of content.

### 3 Jun

- {% badge type="error" text="Bug Fix" /%} **Code Block Saving:** Edits were not saved correctly inside code blocks.
- {% badge type="info" text="Improvement" /%} **Code Block Tabs**: Titled code blocks with no syntax highlighting would still show tab title.

### 2 Jun

- {% badge type="error" text="Bug Fix" /%} **Code Blocks Hiding:** Code blocks contents hide irregularly at some page loads.
- {% badge type="success" text="New" /%} **New Code Language**: Added YAML language.

### 1 Jun

- {% badge type="success" text="New" /%} **Code Languages**: Added Scala, Squirrel and XML. Added HTML as a language (instead of general Markup).
- {% badge type="info" text="Improvement" /%} **Streamlined Coding**: All code blocks are tiny IDEs now with syntax highlighting enabled in edit mode, respect for indentation, key bindings and smarter syntax formatting. Code block changes do not need an extra save click anymore. Syntax highlights where you edit. Pasting code from external sources leaves no extra new lines. 🎉
- {% badge type="success" text="New" /%} **Code Style**: `--code-font`  and `--code-font-size` can be modified using [Custom CSS](/support-center/custom-css) to modify code font and code font-size all around the platform.

### 27 Mar

- {% badge type="warning" text="Change" /%} **Code Font**: Modified the font used for code to be _Roboto Mono_ as it has better compatibility. Inline code also has this font rather than default font.
- {% badge type="info" text="Improvement" /%} **Font Fallback**: Added font fallback for better compatibility.
- {% badge type="info" text="Improvement" /%} **Response Schema colours**: Arrays and files show in purple font colour rather than default black.

### 26 Mar

- {% badge type="info" text="Improvement" /%} **Drag and Drop**: Blocks can be dragged from the {% icon classes="fas fa-arrows-alt" /%} icon.
- {% badge type="info" text="Improvement" /%} **Drag and Drop**: Versions, documentation and references can be dragged from the {% icon classes="fas fa-grip-vertical" /%} icon.
- {% badge type="info" text="Improvement" /%} **Quick Switcher**: Quick switcher orders pages by newer to older for faster search.

### 25 Mar

- {% badge type="info" text="Improvement" /%} **Copy blocks**: Added minimal support for copying blocks between pages or same page.
- {% badge type="info" text="Improvement" /%} **Keyboard accessibility**: More keyboard accessibility support for adding inline blocks, variable listing, page link listing and others.

### 23 May

- {% badge type="success" text="New" /%} **Keyboard Keys**: Add keyboard keys as inline blocks to content {% key key="↵" /%}
- {% badge type="info" text="Improvement" /%} **Inline Blocks**: Easier accessibility using keyboard between selections.
- {% badge type="error" text="Bug Fix" /%} **Icons Rendering**: Icons in editor mode would show invalid after refresh, but fine in live mode.

### 22 May

- {% badge type="success" text="New" /%} **Icons**: Add Font Awesome [icons](/support-center/icons) to content {% icon classes="fas fa-check" /%}

### 20 May

- {% badge type="info" text="Improvement" /%} **Translations**: Added ability to [translate](/support-center/ui-translation) "Next to read" and "Last updated by {{author}} on {{date}}".

### 18 May

- {% badge type="info" text="Improvement" /%} **Security**: Increased key size for project protection for higher security.
- {% badge type="success" text="New" /%} **ZIP mime:** API References handling of ZIP mime type in example responses.
- {% badge type="success" text="New" /%} **Export API**: Projects can be exported using [API](/support-center/api-references#getexports-project) for select plans.

### 17 May

- {% badge type="success" text="New" /%} **Badges**: Add [Badges](/support-center/badges) as inline blocks to your pages.
- {% badge type="error" text="Bug Fix" /%} **Callout Text**: Callout text was unselectable in reader mode.

### 12 May

- {% badge type="error" text="Bug Fix" /%} **Font Picker**: Font picker dialog was not opening.
- {% badge type="error" text="Bug Fix" /%} **Colour Picker**: Colour picker dialog was not functional.

### 6 May

- {% badge type="success" text="New" /%} **Youtube Related Videos**: [Our youtube block](/support-center/videos) now defaults to having `rel=0` parameter on which shows only related videos from the same channel.
- {% badge type="info" text="Improvement" /%} **Compatibility**: Enhanced compatibility for IE9-10 and Safari 10.
- {% badge type="success" text="New" /%} **CSV Support**: Code blocks now support CSV
- {% badge type="success" text="New" /%} **Reference CSV Support**: References now show CSV responses correctly.
- {% badge type="success" text="New" /%} **Quick Switcher button:** Quick switcher button shows in the left-bottom corner.
- {% badge type="error" text="Bug Fix" /%} **Inline Code:** Inline code using toolbar was broken.

### 3 May

- {% badge type="info" text="Improvement" /%} **We are faster**: Loading DeveloperHub should be 15% faster now!

### 27 Apr

- {% badge type="success" text="New" /%} **Quick Switcher**: Find your pages faster with our [quick switcher](/support-center/quick-switcher) by clicking `⌘/Ctrl`  + `K`. Check the [keyboard shortcuts](/support-center/keyboard-shortcuts).

### 26 Apr

- {% badge type="success" text="New" /%} **Validate OpenAPI**: We started validating strictly the OpenAPI spec you upload, and return the validation errors if any in the platform.
- {% badge type="success" text="New" /%} **Page Linking - Keyboard Shortcut**: You can now move up/down with keyboard when selecting a page to link.
- {% badge type="error" text="Bug Fix" /%} **(+) not showing:** Whenever you're on an empty line, the (+) for adding blocks will show now.

### 25 Apr

- {% badge type="error" text="Bug Fix" /%} **Table of Contents**: Previously, table of contents could collapse below content when a big table is in the page between 1250px-1300px window width.

### 23 Apr

- {% badge type="success" text="New" /%} **UI Translation**: Translate the [UI text](/support-center/ui-translation).
- {% badge type="error" text="Bug Fix" /%} **Importing tables**: Importing tables containing markdown does not show HTML tags anymore.

### 21 Apr

- {% badge type="success" text="New" /%} **Headings linking**: On linking pages, headings show in the list to link to a [specific heading](/support-center/page-linking#changing-link-title-specifying-heading). Previously, you'd have to get the heading fragment from the URL.

### 20 Apr

- {% badge type="success" text="New" /%} **Lists in Tables**: Tables support Markdown notation for lists.

### 13 Apr

- {% badge type="success" text="New" /%} **Exporting Tables Modified**: HTML will be stripped out of any exported table. Markdown will be preserved.

### 10 Apr

- {% badge type="success" text="New" /%} **Custom Landing Page**: Craft your own [custom landing page](/support-center/custom-landing-page).

### 9 Apr

- {% badge type="warning" text="Change" /%} **Important CSS Change**: Modified `.card` in our landing page CSS into `.landing-card`. Please make the needed modifications if you use this selector.

### 30 Mar

- {% badge type="success" text="New" /%} **Pascal support**: Code blocks now support Pascal.

### 29 Mar

- {% badge type="success" text="New" /%} **Titled code blocks**: Add titles to your [code blocks](/support-center/code-blocks) to indicate content regardless of code language.

### 28 Mar

- {% badge type="success" text="New" /%} **Show page updates**: Your readers can now check at the bottom of each page when the page was last updated and by whom. Enable this through Documentation Settings.


{% image url="https://uploads.developerhub.io/prod/02/hykd48w00eyt5cicsd37zyxlhpmcoae3ls99t0wapmix5b4un3ikvah6k8uwyq37.jpg" caption="" mode="responsive" height="77" width="295" %}
{% /image %}


### 23 Feb

- {% badge type="info" text="Improvement" /%} **Better Slack notifications**: Slack notifications are grouped by documentation.
- {% badge type="success" text="New" /%} **Documentation slug**: Documentation slug can now be changed from Documentation settings.
- {% badge type="info" text="Improvement" /%} **Tables export**: When tables are now exported, they are in Markdown format rather than HTML.
- {% badge type="error" text="Bug Fix" /%} **Deletion**: Previously deleting a project, version, documentation or page could fail when there are comments.

### 13 Jan

- {% badge type="success" text="New" /%} **Disable live markdown rendering**: Disable live markdown rendering if you wish, in case you're placing too many underscores in variable names, for example.
