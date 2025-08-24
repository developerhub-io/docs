---
type: page
title: 2021 Updates
listed: true
slug: 2021-updates
description: 
index_title: 2021 Updates
hidden: 
keywords: 
tags: 
---

### 27 Dec

- {% badge type="success" text="New" /%} **API Reference**: Support for `deprecated` on operations.

### 19 Dec

- {% badge type="success" text="New" /%} **API Reference**: Added support for Terms of Service and License.
- {% badge type="success" text="New" /%} **API Reference**: We now show the API version next to the name.
- {% badge type="success" text="New" /%} **API Reference**: Added support for named request examples of OAS3.
- {% badge type="warning" text="Change" /%} **Code Block**: On mobile displays, code lines will not wrap anymore so lines do not get cluttered.

### 16 Dec

- {% badge type="success" text="New" /%} **Variables**: Allow exposing variables to `window` object for use in [Custom HEAD Tags](/support-center/custom-javascript).
- {% badge type="success" text="New" /%} **Scripts/Styles**: Allow disabling [scripts](/support-center/custom-javascript#disabling-head-tags) and [styles](/support-center/custom-css#disabling-styles) through URL for testing purposes.

### 11 Dec

- {% badge type="error" text="Bug Fix" /%} **Tables**: Links having quotations in table paragraphs were not showing correctly after multiple edits.

### 08 Dec

- {% badge type="warning" text="Change" /%} **Team**: Default role for newly invited teammates is now Publisher instead of Admin.

### 03 Dec

- {% badge type="success" text="New" /%} **API Reference**: Added support for the following constraints: `maxLength`, `minLength`, `pattern`, `minimum`, `maximum` and `multipleOf`.

### 02 Dec

- {% badge type="success" text="New" /%} **API**: Added an API to find a page using slugs [GET - Get page by slug](/api/ref#get-page).
- {% badge type="success" text="New" /%} **API Reference**: Show enums for fields under request parameters

### 01 Dec

- {% badge type="error" text="Bug Fix" /%} **Editor**: Inline code having backticks was losing formatting after two page saves.
- {% badge type="info" text="Improvement" /%} **Editor**: Handling getting out of inline code just became much better when hitting right arrow or enter.

### 29 Nov

- {% badge type="info" text="Improvement" /%} **API**: Page IDs are now shown in the UI under the page title at Sidebar &gt; Page for your use on our [APIs](/api/ref).

### 28 Nov

- {% badge type="error" text="Bug Fix" /%} **Images**: Fixed bug where pasting images does not create an [image](/support-center/images) block.

### 27 Nov

- {% badge type="success" text="New" /%} **API References**: Added support for multiple server URLs.

### 24 Nov

- {% badge type="success" text="New" /%} **Custom HEAD Tags**: `onprojectloaded` event gets triggered which lets you know when you can start modifying the layout of the docs.

### 22 Nov

- {% badge type="success" text="New" /%} **Templates**: Ability to start from a template directly using [template links](/support-center/templates#share-a-template-link).

### 18 Nov

- {% badge type="success" text="New" /%} **Synced Blocks**: Reuse content with [auto$](/support-center/synced-blocks).
- {% badge type="info" text="Improvement" /%} **Blocks**: All margins for blocks have been standardised for a more consistent look.
- {% badge type="info" text="Improvement" /%} **Templates**: Choose templates from a form that displays all the templates available including their content, rather than from a dropdown.
- {% badge type="warning" text="Change" /%} **API**: `entityId` of [GET - Get audit log](/api/ref#get-audit-log) is a string, no longer an integer.

### 16 Nov

- {% badge type="error" text="Bug Fix" /%} **PDF Exports**: Errors preventing PDF generation were not showing, if any.
- {% badge type="error" text="Bug Fix" /%} **PDF Exports**: Exports used to break if there was an empty documentation.

### 15 Nov

- {% badge type="success" text="New" /%} **API References**: Added support for `readOnly` and `writeOnly`.

### 11 Nov

- {% badge type="success" text="New" /%} **API References**: Callbacks support.

### 09 Nov

- {% badge type="success" text="New" /%} **Custom HTML**: Added [Jupyter Notebook](/support-center/jupyter-notebook-integration) embedding instructions.
- {% badge type="success" text="New" /%} **API**: Added an API to [update pages](/api/ref#update-page).
- {% badge type="warning" text="Change" /%} **API**: [Search Content API](/api/ref#search) now also provides pageId in addition to the page name.
- {% badge type="error" text="Bug Fix" /%} **Custom HTML**: Styles are no longer removed, but instead the Custom HTML contents would be enclosed in an iFrame.

### 05 Nov

- {% badge type="success" text="New" /%} **API Reference**: Show OpenIDConnectURL for OpenID authentication schemes.
- {% badge type="error" text="Bug Fix" /%} **Version Picker**: Version and section pickers used to show text cursor instead of pointer.

### 27 Oct

- {% badge type="warning" text="Change" /%} **Custom Login**: Variables are now [injected](/support-center/custom-login) in a `vars` object under `payload`.
- {% badge type="error" text="Bug Fix" /%} **Quick Switcher**: Opening [Quick Switcher](/support-center/quick-switcher) before a version has loaded used to break the search.

### 26 Oct

- {% badge type="info" text="Improvement" /%} **Performance**: Loading time for projects in the editor exponentially decreased for projects with many versions.
- {% badge type="info" text="Improvement" /%} **SEO**: Robots hitting non-existent links will get 404.
- {% badge type="warning" text="Change" /%} **Quick Search**: Editor option to search through all versions is removed momentarily.

### 23 Oct

- {% badge type="error" text="Bug Fix" /%} **CSS**: Right sidebar was falling below the search bar.

### 16 Oct

- {% badge type="success" text="New" /%} **Invoices**: View invoices and [update billing details](/support-center/supercharged-plans#changing-paymentbilling-details) easily.

### 14 Oct

- {% badge type="error" text="Bug Fix" /%} **Mobile Layout**: Index dropdown button and feedback controls were not aligned perfectly.

### 07 Oct

- {% badge type="success" text="New" /%} **CSS**: [Test CSS changes](/support-center/custom-css#testing-css) before deploying them to your readers.
- {% badge type="error" text="Bug Fix" /%} **Callout**: Icons and badges in callouts were not being saved correctly.

### 06 Oct

- {% badge type="error" text="Bug Fix" /%} **Variables**: Variables were not getting applied in code blocks.
- {% badge type="error" text="Bug Fix" /%} **Landing Page**: Google analytics was not always firing event for landing page when returning from a page.
- {% badge type="error" text="Bug Fix" /%} **Landing Page**: Browser URL when returning to landing page from a page was not updating.

### 04 Oct

- {% badge type="error" text="Bug Fix" /%} **Blocks**: Adding blocks was not possible using the + sign on an empty line.

### 03 Oct

- {% badge type="success" text="New" /%} **Templates**: Create page [templates](/support-center/templates) and apply on new pages.
- {% badge type="warning" text="Change" /%} **CSS**: Huge changes of how the editor is integrated were made (so we can enable further features), which lead to some CSS changes. CSS selectors which you might want to double check: `app-documentation-content`, `.master >` and `.master-content`.

### 20 Sep

- {% badge type="success" text="New" /%} **Embed**: A non-minimal [embed mode](/support-center/previewing-documentation#embed-mode) is now available.

### 14 Sep

- {% badge type="success" text="New" /%} **Search Analytics**: Enterprise accounts can setup [enterprise search](/support-center/enterprise-search) analytics to segment data from different projects.

### 13 Sep

- {% badge type="error" text="Security" /%} **TLS**: All our assets are now served over TLS 1.2 instead of TLS 1.1.

### 10 Sep

- {% badge type="warning" text="Change" /%} **Code Blocks**: Code blocks automatically collapse if it is larger than 100 lines. We also now expand the first line now rather than folding all lines.
- {% badge type="info" text="Improvement" /%} **Embed Mode**: Table of contents and index are automatically hidden.

### 08 Sep

- {% badge type="success" text="New" /%} **API Reference**: Can use OpenAPI native variables in Server URL, as well as our own [variables](/support-center/variables).
- {% badge type="success" text="New" /%} **API**: Two new APIs to [create a page](/api/ref#create-page) and [publish a page](/api/ref#publish-page).

### 07 Sep

- {% badge type="success" text="New" /%} **Page History**: Page history now follows through pages in cloned versions. This means that the creators and contributors will not be lost when a page is cloned, and that you'll be able to access previous versions from the cloned page as well as the original page.

### 06 Sep

- {% badge type="success" text="New" /%} **Page Linking**: After choosing an API reference when page linking, you are now provided with a list of the operations for you to link to directly, rather than having to figure out the URL fragment.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Fix to request bodies with root oneOf/anyOf not showing the table.

### 31 Aug

- {% badge type="success" text="New" /%} **API Reference**: Nested oneOf/anyOf in request body now supported.
- {% badge type="error" text="Bug Fix" /%} **Version Cloning**: Some documentation settings were not cloned to the new documentation when a version is cloned.

### 27 Aug

- {% badge type="success" text="New" /%} **Search Engine**: Setup your docs site as a [search engine](/support-center/using-search#searching-using-url) on browsers.

### 26 Aug

- {% badge type="success" text="New" /%} **PDF Export**: Enterprise customers can [export an entire version to PDF](/support-center/pdf-export).

### 20 Aug

- {% badge type="success" text="New" /%} **Page Details**: See page creator from Sidebar &gt; Page.

### 13 Aug

- {% badge type="error" text="Bug Fix" /%} **Font**: Custom landing pages did not inherit the project font by default.

### 11 Aug

- {% badge type="success" text="New" /%} **Search**: Enabled [advanced search operators](/support-center/using-search#advanced-search-operators) for our lightning-fast search.
- {% badge type="error" text="Bug Fix" /%} **API References**: No longer show a collapsed table when `requestBody` is defined but empty.

### 10 Aug

- {% badge type="success" text="New" /%} **Read Page API**: Added an [API](/api/ref#read-page) to read pages in [Darkdown](/support-center/exporting-documentation#darkdown) or text format.
- {% badge type="success" text="New" /%} **Users**: Search through the team members list by name/email.

### 09 Aug

- {% badge type="error" text="Bug Fix" /%} **Page Linking**: Links with specified titles having commas were causing the browser to hang.

### 07 Aug

- {% badge type="success" text="New" /%} **Organisation Search**: Multi project search in a list fashion is available now for Enterprise plans.

### 29 Jul

- {% badge type="success" text="New" /%} **API**: New [API](/api/ref) available to update version which allows you to publish and unpublish a version programmatically.
- {% badge type="success" text="New" /%} **Re-ordering Index**: Re-arrange elements in a big index fast by entering the menu, click Re-arrange, and choosing a category to move it to.

### 26 Jul

- {% badge type="error" text="Bug Fix" /%} **Password Protection**: Minority of customers who set up passwords before 2020 were unable to access anymore using the secure links they previously generated due to deprecation of the old system. The old system has been recovered now.

### 25 Jul

- {% badge type="success" text="New" /%} **JWT authentication**: Use [custom login](/support-center/custom-login) through JWT to log in your readers and [personalise](/support-center/personalised-docs) their docs.

### 20 Jul

- {% badge type="success" text="New" /%} **Documentation Settings**: You can now only [show the date](/support-center/documentation-settings#show-page-last-updated) without the author in "Last Page Updated" section at the bottom of the page, without needing to modify CSS.
- {% badge type="success" text="New" /%} **Formatting**: External links will now show a top-right pointing arrow in editor mode to indicate that they are external links, not [internal links](/support-center/page-linking).
- {% badge type="error" text="Bug Fix" /%} **Audit**: Deleting version was spamming the audit log with multiple entries.

### 13 Jul

- {% badge type="error" text="Bug Fix" /%} **Search**: Search could fail due to expired search token if a user does not visit the landing page after the search token expires.

### 12 Jul

- {% badge type="success" text="New" /%} **Hosting**: [Host multiple projects](/support-center/hosting#hosting-multiple-projects-under-one-site) under the same subdomain or custom domain.
- {% badge type="error" text="Bug Fix" /%} **Landing Page**: Clicking on the logo to go to landing page did not change the URL.

### 29 Jun

- {% badge type="error" text="Bug Fix" /%} **Import/Export**: Further fixes to new lines import/export for tables, as well as supporting new lines in table headers when importing.

### 23 Jun

- {% badge type="success" text="New" /%} **Formatting**: Heading 4 is now available through all the different methods of [formatting](/support-center/formatting-text).
- {% badge type="success" text="New" /%} **UI Translation**: French is now available as a pre-defined [UI language](/support-center/ui-translation).

### 21 Jun

- {% badge type="error" text="Bug Fix" /%} **Import/Export**: Text between tags in tables was not exporting/importing correctly.

### 16 Jun

- {% badge type="success" text="New" /%} **History**: We'll calculate and show you how many lines changed on every change so you know which edits are more signifcant.

### 15 Jun

- {% badge type="info" text="Improvement" /%} **Import**: You no longer need to remove HTML tags when importing, we will sanitise it for you.
- {% badge type="error" text="Bug Fix" /%} **Pasting**: Pasting images was not working with Chrome latest update.

### 13 Jun

- {% badge type="success" text="New" /%} **Hosting**: Host your docs in a [subdirectory under your existing website](/support-center/hosting#hosting-under-an-existing-website).
- {% badge type="success" text="New" /%} **Linked Pages**: View the [pages linking](/support-center/page-linking#listing-linked-pages) to any page.

### 22 May

- {% badge type="error" text="Security" /%} **TLS**: Dropped support for the deprecated TLSv1.0 and TLSv1.1.

### 20 May

- {% badge type="success" text="New" /%} **Localisation**: We added a guide for [localisation](/support-center/localisation).
- {% badge type="success" text="New" /%} **Formatting**: Ordered lists now show different list type so you can reference items better, such as:
    1. This is first item, uses numbering.
        1. This is second item, uses lower alpha.
            1. This is third item, uses lower roman letters.

- {% badge type="success" text="New" /%} **Quick Search**: Option to only search through current version.
- {% badge type="success" text="New" /%} **User Images**: If you sign in with Google, you'll get your profile picture added on DeveloperHub.
- {% badge type="info" text="Improvement" /%} **SSO**: If you're an SSO user on Google SAML, then if you click on Sign in using Google, we'll automatically sign you in using SSO.
- {% badge type="info" text="Improvement" /%} **Go To**: Go To button now would not add the version slug if you were on the default version.

### 18 May

- {% badge type="success" text="New" /%} **Logout**: When your logged in session expires, you can now log in back without losing what you're working on.
- {% badge type="error" text="Security" /%} **Feedback**: XSS was possible through feedback message input. Feedback messages can no longer have markdown, as it is also a bit of an overkill.

### 17 May

- {% badge type="success" text="New" /%} **SEO**: To disable search engine indexing, you can do it now from Project Settings directly.
- {% badge type="success" text="New" /%} **SEO**: There are now [Advanced Settings](/support-center/advanced-settings) to canonicalise URLs without version slug for the default version, as well as to prevent indexing for older versions.
- {% badge type="error" text="Bug Fix" /%} **Access**: Projects using custom domains were unable to load due to a security rule change. All functionality has been returned to normal now.

### 16 May

- {% badge type="success" text="New" /%} **Images**: You can upload images directly by pasting them.
- {% badge type="success" text="New" /%} **Version Banner**: Added an [advanced setting](/support-center/advanced-settings) to show a banner when the reader is viewing an older version.
- {% badge type="info" text="Improvement" /%} **Formatting**: Place cursor correctly after outdenting a list.

### 14 May

- {% badge type="success" text="New" /%} **Formatting**: Nested lists are now supported!
- {% badge type="success" text="New" /%} **Formatting**: Continue numbering for ordered lists (only for first level).

### 9 May

- {% badge type="warning" text="Change" /%} **CSS**: Removed footer default margin.

### 3 May

- {% badge type="success" text="New" /%} **Feedback**: [Feedback](/support-center/feedback) is now enabled by default for all new projects.
- {% badge type="error" text="Bug Fix" /%} **Links**: Having commas in the title of a link used to break a link.

### 29 Apr

- {% badge type="success" text="New" /%} **Slack Feedback**: [Feedback](/support-center/feedback) is now sent to [Slack](/support-center/slack).

### 25 Apr

- {% badge type="success" text="New" /%} **Feedback**: Gather [feedback](/support-center/feedback) from your readers right from the pages.
- {% badge type="warning" text="Change" /%} **Search Analytics**: Increase viewable analytics range to 30 days from 14 days.

### 15 Apr

- {% badge type="success" text="New" /%} **Cookie Consent**: Cookie consent text can now be changed.
- {% badge type="warning" text="Change" /%} **API References**: Show "No Scopes" for OAuth2 flows with no scopes, and multiple CSS changes for OAuth2 definitions.

### 12 Apr

- {% badge type="success" text="New" /%} **Open in Editor**: An edit button will be shown at the bottom right of your live docs when you use any of our Go To buttons in the sidebar.

### 10 Apr

- {% badge type="success" text="New" /%} **Require Annotation**: Added a [project setting](/support-center/advanced-settings) to require that editors annotate changes.
- {% badge type="success" text="New" /%} **Open in Editor**: Added a [keyboard shortcut](/support-center/keyboard-shortcuts) to open pages in editor when in live mode.

### 3 Apr

- {% badge type="success" text="New" /%} **Search Analytics:** Find out how your readers are using search using [Search Analytics](/support-center/search-analytics).
- {% badge type="success" text="New" /%} **Page Contributors**: Find the list of contributors on a page from Page details menu.
- {% badge type="error" text="Bug Fix" /%} **Index**: Index rarely went out of sync, but no more.

### 1 Apr

- {% badge type="error" text="Bug Fix" /%} **Index**: Drag/drop was too slow for big documentation. Now it is as fast as a one-page documentation!

### 31 Mar

- {% badge type="info" text="Improvement" /%} **Import**: Clarify the error when a parent page is expected to exist but does not.

### 29 Mar

- {% badge type="error" text="Bug Fix" /%} **Cloning**: Version cloning was failing if there is an API Reference in the version.

### 28 Mar

- {% badge type="success" text="New" /%} **Lock pages when editing**: Added a project setting to [lock page](/support-center/advanced-settings#lock-page-when-editing) when editing to ensure data does not get overwritten by multiple people editing at the same time.

### 27 Mar

- {% badge type="success" text="New" /%} **User images**: For your user profiles, you can now show your profile photo using [Gravatar](https://gravatar.com/).

### 25 Mar

- {% badge type="info" text="Improvement" /%} **Performance**: Loading project for your readers just went 4x faster for smaller projects and 10x faster larger projects 🔥
- {% badge type="success" text="New" /%} **API Reference**: Ability to change the API Reference slug.

### 22 Mar

- {% badge type="success" text="New" /%} **Code Theme**: Use other CodeMirror [code themes](/support-center/code-theme).

### 17 Mar

- {% badge type="success" text="New" /%} **Personalise Docs**: Personalise the docs using [injected variables](/support-center/variables#personalise-docs).
- {% badge type="info" text="Improvement" /%} **Editor**: Editor loading is now much faster for users with multiple projects.
- {% badge type="warning" text="Change" /%} **API References**: Disabled breaking words in tables.

### 16 Mar

- {% badge type="success" text="New" /%} **API References**: Added Java OkHttp to [available libraries](/support-center/code-generation#available-libraries) for generating example requests.
- {% badge type="success" text="New" /%} **Annotate History**: Add a message to page history to indicate what the change was.

### 10 Mar

- {% badge type="success" text="New" /%} **Image**: Zoom image on click.
- {% badge type="error" text="Bug Fix" /%} **Table Resizing**: Resizing grips were not showing when the column head had formatting.

### 8 Mar

- {% badge type="success" text="New" /%} **Duplicate Index**: Duplicate pages, links, separators and categories right away from the index.
- {% badge type="success" text="New" /%} **CSS**: Added `active-category` class to the currently active category.

### 5 Mar

- {% badge type="success" text="New" /%} **SSO**: [Sign in](/support-center/editor-single-sign-on--sso-) your users through your Identity Provider (IdP).

### 27 Feb

- {% badge type="warning" text="Improvement" /%} **Cloning**: When cloning a version, if any page had raw HTML, you will now be informed of the page title and documentation title of the offending page.

### 25 Feb

- {% badge type="error" text="Bug Fix" /%} **Editing**: Writing HTML tag-like text in a page no longer can cause unexpected page rendering, such as &lt;script&gt;, &lt;tag&gt; or else.
- {% badge type="warning" text="Improvement" /%} **General**: You can no longer move from a page with unsaved changes in any way without confirmation

### 22 Feb

- {% badge type="success" text="New" /%} **API References**: Support for generating examples for arrays as well as array items.
- {% badge type="error" text="Bug Fix" /%} **API References**: Description was showing as `default` for requests.

### 20 Feb

- {% badge type="success" text="New" /%} **Tables**: Table columns are now resizable.

### 18 Feb

- {% badge type="success" text="New" /%} **API References**: Added support for `default` in parameters.
- {% badge type="warning" text="Change" /%} **API References**: No longer show headers table if there are no headers.
- {% badge type="warning" text="Change" /%} **API References**: Enhanced design for `enum`  and `default` rendering.
- {% badge type="error" text="Bug Fix" /%} **API References**: Fix to choosing OpenAPI-wide security schemes over operation overrides.
- {% badge type="error" text="Bug Fix" /%} **Index**: When creating a page, the index scroll used to go back to the top.

### 17 Feb

- {% badge type="success" text="New" /%} **API References**: Show request body description for requests, if any.

### 16 Feb

- {% badge type="success" text="New" /%} **API References**: Headers and queries for the selected security scheme now shows in the example request.
- {% badge type="error" text="Bug Fix" /%} **Import**: When an import file has two identical blocks, they used get associated to each other.

### 14 Feb

- {% badge type="warning" text="Change" /%} **CSS**: Font weight for inline code changed to 400 instead of 500. You can revert this change for your project by using `.customise .inline-code{ font-weight: var(--fw-500); }`.

### 9 Feb

- {% badge type="success" text="New" /%} **SEO**: On pasting a documentation link on a social platform/slack/etc..., we'll preview the best image and description of the content possible.
- {% badge type="success" text="New" /%} **API References**: Show response headers under responses.
- {% badge type="success" text="New" /%} **API References**: Added C# HttpClient to [available libraries](/support-center/code-generation#available-libraries) for generation request examples.
- {% badge type="success" text="New" /%} **API References CSS**: Add CSS selectors for each field in the tables.

### 8 Feb

- {% badge type="warning" text="Change" /%} **Font**: We have changed the default font to [Nunito](https://fonts.google.com/specimen/Nunito).
- {% badge type="success" text="New" /%} **Font**: Customise [font weights](/support-center/custom-css#font-weights) for your font.

### 6 Feb

- {% badge type="success" text="New" /%} **API References**: Allow tags to [expand](/support-center/api-reference-settings#allow-tags-to-be-expand).
- {% badge type="success" text="New" /%} **API References**: Show endpoint operations next to tags when expandable.
- {% badge type="success" text="New" /%} **API References**: Show enums for properties.
- {% badge type="success" text="New" /%} **API References**: Tag links in the index are now clickable.
- {% badge type="success" text="New" /%} **API References**: Request and response examples follow scrolling, making it easier for the reader to find the information they need.
- {% badge type="error" text="Bug Fix" /%} **Favicon**: DeveloperHub icon no longer loads by default.
- {% badge type="warning" text="Change" /%} **API References**: CSS makeover, larger titles, more space.

### 4 Feb

- {% badge type="error" text="Bug Fix" /%} **API References**: Fix example request hidden when request body has examples.
- {% badge type="error" text="Bug Fix" /%} **API References**: All Go net/http were showing as GET requests in examples.
- {% badge type="error" text="Bug Fix" /%} **API References**: Response body used to show the array item title as the title of the object.

### 3 Feb

- {% badge type="success" text="New" /%} **API References**: Go net/http and PHP Guzzle are now available as [libraries](/support-center/code-generation#available-libraries) for generated request examples.
- {% badge type="success" text="New" /%} **Search**: Search can now be opened using {% key key="⌘" /%}/{% key key="Ctrl" /%} + K for readers.
- {% badge type="warning" text="Change" /%} **Code Generation**: Removed ability to choose which libraries are seen by your users. Majority of API References had all libraries enabled.
- {% badge type="error" text="Bug Fix" /%} **API References**: Request and responses `examples`  included the key `value`. Now it's removed.

### 2 Feb

- {% badge type="success" text="New" /%} **Help & Support**: New Help & Support menu to reach our [community discussions](https://talk.developerhub.io), report bugs and submit feature requests.
- {% badge type="success" text="New" /%} **API References**: Requests have support for example under oneOf, anyOf, allOf.
- {% badge type="success" text="New" /%} **API References**: Requests have support for showing the first example of examples.
- {% badge type="success" text="New" /%} **API References**: Responses have support for showing all examples and having them selectable.
- {% badge type="error" text="Bug Fix" /%} **API References**: Requests and responses that have an array of undefined type would show just `array` instead of `array[undefined]`.
- {% badge type="error" text="Bug Fix" /%} **API References**: Requests object title was not shown.
- {% badge type="error" text="Bug Fix" /%} **API References**: Markdown rendering for big images could have overflowed the container.

### 31 Jan

- {% badge type="success" text="New" /%} **Edit History**: [Edit history](/support-center/page-history) now shows the differences in colours. You can also see the change between current edit and the published edit. Along that, we redesigned a bit the page history panel to focus on published edits rather than drafts.
- {% badge type="error" text="Bug Fix" /%} **Import/Export**: We no longer show import/export options when viewing a page edit history as it was misleading.
- {% badge type="error" text="Bug Fix" /%} **Dashboard**: Comment list was not scrollable if too long.
- {% badge type="error" text="Bug Fix" /%} **Compatibility**: On Safari, project logo width could be miscalculated on same loads causing search bar to fall.

### 27 Jan

- {% badge type="error" text="Bug Fix" /%} **Activity Log**: On reordering indices, there was no icon or good explanation of what happened.
- {% badge type="error" text="Bug Fix" /%} **API References**: Fields other than Operation Objects under Path Item Object used to break an API reference.

### 24 Jan

- {% badge type="success" text="New" /%} **Audit**: Enterprise customers can query [audit logs](/support-center/activity-log#enterprise-auditing) using the [API](/api/ref#get-activity-log).
- {% badge type="success" text="New" /%} **Get All**: All users can query all resources on %product% using [API](/api/ref#all-project).
- {% badge type="warning" text="Change" /%} **API Rate Limits**: All APIs are rate limited.

### 19 Jan

- {% badge type="success" text="New" /%} **Publishing**: Added a [setting](/support-center/advanced-settings#ask-before-publishing) to prompt you if you are publishing a page that has unresolved comments.
- {% badge type="success" text="New" /%} **Comments**: You can now [resolve](/support-center/comments#resolve-comments) all comments on a page from the activity bar.
- {% badge type="warning" text="Improvement" /%} **Page Linking**: Search for page linking after typing "@" now searches through titles and slugs. It also tolerates typos.

### 16 Jan

- {% badge type="error" text="Bug Fix" /%} **Blocks**: Duplicating a block more than once at the same time used to have unexpected results.
- {% badge type="error" text="Bug Fix" /%} **Table**: The floating table options control used to float at the wrong place if a row had multiline input.

### 12 Jan

- {% badge type="success" text="New" /%} **Activity Log**: View the latest changes right away from the [dashboard](/support-center/dashboard).
- {% badge type="warning" text="Improvement" /%} **Heading Selection**: When linking a page, we'll automatically copy the heading title if a heading was selected and no title was chosen yet.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: API References were not delete-able from 11 Jan 2021.
- {% badge type="error" text="Bug Fix" /%} **Import**: In case of an incomplete import due to error, we now delete the incomplete versions.

### 11 Jan

- {% badge type="success" text="New" /%} **CSS Changes**: Added a CSS selector to apply CSS to select versions.

### 8 Jan

- {% badge type="success" text="New" /%} **Embed Mode**: Add `?goto=embed` when navigating to a page to enable [embed mode](/support-center/previewing-documentation#embed-mode).

### 7 Jan

- {% badge type="warning" text="Change" /%} **User Roles**: Publishers can no longer change project colours or top navigation links/icons.
- {% badge type="error" text="Bug Fix" /%} **Colour Picker**: On opening the picker, it used to default colours even if settings were not explicitly changed.
