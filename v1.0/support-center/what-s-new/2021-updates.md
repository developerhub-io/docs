---
type: page
title: 2021 Updates
listed: true
description: 
index_title: 2021 Updates
hidden: false
keywords: 
tags: 
---

### 27 Dec

- {% badge text="New" type="success" /%} **API Reference**: Support for `deprecated` on operations.

### 19 Dec

- {% badge text="New" type="success" /%} **API Reference**: Added support for Terms of Service and License.
- {% badge text="New" type="success" /%} **API Reference**: We now show the API version next to the name.
- {% badge text="New" type="success" /%} **API Reference**: Added support for named request examples of OAS3.
- {% badge text="Change" type="warning" /%} **Code Block**: On mobile displays, code lines will not wrap anymore so lines do not get cluttered.

### 16 Dec

- {% badge text="New" type="success" /%} **Variables**: Allow exposing variables to `window` object for use in [Custom HEAD Tags](../custom-javascript.md).
- {% badge text="New" type="success" /%} **Scripts/Styles**: Allow disabling [scripts](../custom-javascript.md#disabling-head-tags) and [styles](../customising-visuals/custom-css.md#disabling-styles) through URL for testing purposes.

### 11 Dec

- {% badge text="Bug Fix" type="error" /%} **Tables**: Links having quotations in table paragraphs were not showing correctly after multiple edits.

### 08 Dec

- {% badge text="Change" type="warning" /%} **Team**: Default role for newly invited teammates is now Publisher instead of Admin.

### 03 Dec

- {% badge text="New" type="success" /%} **API Reference**: Added support for the following constraints: `maxLength`, `minLength`, `pattern`, `minimum`, `maximum` and `multipleOf`.

### 02 Dec

- {% badge text="New" type="success" /%} **API**: Added an API to find a page using slugs [GET - Get page by slug](/api/ref#get-page).
- {% badge text="New" type="success" /%} **API Reference**: Show enums for fields under request parameters

### 01 Dec

- {% badge text="Bug Fix" type="error" /%} **Editor**: Inline code having backticks was losing formatting after two page saves.
- {% badge text="Improvement" /%} **Editor**: Handling getting out of inline code just became much better when hitting right arrow or enter.

### 29 Nov

- {% badge text="Improvement" /%} **API**: Page IDs are now shown in the UI under the page title at Sidebar \> Page for your use on our [APIs](/api/ref).

### 28 Nov

- {% badge text="Bug Fix" type="error" /%} **Images**: Fixed bug where pasting images does not create an [image](../images.md) block.

### 27 Nov

- {% badge text="New" type="success" /%} **API References**: Added support for multiple server URLs.

### 24 Nov

- {% badge text="New" type="success" /%} **Custom HEAD Tags**: `onprojectloaded` event gets triggered which lets you know when you can start modifying the layout of the docs.

### 22 Nov

- {% badge text="New" type="success" /%} **Templates**: Ability to start from a template directly using [template links](../templates.md#share-a-template-link).

### 18 Nov

- {% badge text="New" type="success" /%} **Synced Blocks**: Reuse content with [Synced Blocks](../synced-blocks.md).
- {% badge text="Improvement" /%} **Blocks**: All margins for blocks have been standardised for a more consistent look.
- {% badge text="Improvement" /%} **Templates**: Choose templates from a form that displays all the templates available including their content, rather than from a dropdown.
- {% badge text="Change" type="warning" /%} **API**: `entityId` of [GET - Get audit log](/api/ref#get-audit-log) is a string, no longer an integer.

### 16 Nov

- {% badge text="Bug Fix" type="error" /%} **PDF Exports**: Errors preventing PDF generation were not showing, if any.
- {% badge text="Bug Fix" type="error" /%} **PDF Exports**: Exports used to break if there was an empty documentation.

### 15 Nov

- {% badge text="New" type="success" /%} **API References**: Added support for `readOnly` and `writeOnly`.

### 11 Nov

- {% badge text="New" type="success" /%} **API References**: Callbacks support.

### 09 Nov

- {% badge text="New" type="success" /%} **Custom HTML**: Added [Jupyter Notebook](../integrations/jupyter-notebook-integration.md) embedding instructions.
- {% badge text="New" type="success" /%} **API**: Added an API to [update pages](/api/ref#update-page).
- {% badge text="Change" type="warning" /%} **API**: [Search Content API](/api/ref#search) now also provides pageId in addition to the page name.
- {% badge text="Bug Fix" type="error" /%} **Custom HTML**: Styles are no longer removed, but instead the Custom HTML contents would be enclosed in an iFrame.

### 05 Nov

- {% badge text="New" type="success" /%} **API Reference**: Show OpenIDConnectURL for OpenID authentication schemes.
- {% badge text="Bug Fix" type="error" /%} **Version Picker**: Version and section pickers used to show text cursor instead of pointer.

### 27 Oct

- {% badge text="Change" type="warning" /%} **Custom Login**: Variables are now [injected](../private-docs/custom-login.md) in a `vars` object under `payload`.
- {% badge text="Bug Fix" type="error" /%} **Quick Switcher**: Opening [Quick Switcher](../quick-switcher.md) before a version has loaded used to break the search.

### 26 Oct

- {% badge text="Improvement" /%} **Performance**: Loading time for projects in the editor exponentially decreased for projects with many versions.
- {% badge text="Improvement" /%} **SEO**: Robots hitting non-existent links will get 404.
- {% badge text="Change" type="warning" /%} **Quick Search**: Editor option to search through all versions is removed momentarily.

### 23 Oct

- {% badge text="Bug Fix" type="error" /%} **CSS**: Right sidebar was falling below the search bar.

### 16 Oct

- {% badge text="New" type="success" /%} **Invoices**: View invoices and [update billing details](../supercharged-plans.md#changing-paymentbilling-details) easily.

### 14 Oct

- {% badge text="Bug Fix" type="error" /%} **Mobile Layout**: Index dropdown button and feedback controls were not aligned perfectly.

### 07 Oct

- {% badge text="New" type="success" /%} **CSS**: [Test CSS changes](../customising-visuals/custom-css.md#testing-css) before deploying them to your readers.
- {% badge text="Bug Fix" type="error" /%} **Callout**: Icons and badges in callouts were not being saved correctly.

### 06 Oct

- {% badge text="Bug Fix" type="error" /%} **Variables**: Variables were not getting applied in code blocks.
- {% badge text="Bug Fix" type="error" /%} **Landing Page**: Google analytics was not always firing event for landing page when returning from a page.
- {% badge text="Bug Fix" type="error" /%} **Landing Page**: Browser URL when returning to landing page from a page was not updating.

### 04 Oct

- {% badge text="Bug Fix" type="error" /%} **Blocks**: Adding blocks was not possible using the + sign on an empty line.

### 03 Oct

- {% badge text="New" type="success" /%} **Templates**: Create page [templates](../templates.md) and apply on new pages.
- {% badge text="Change" type="warning" /%} **CSS**: Huge changes of how the editor is integrated were made (so we can enable further features), which lead to some CSS changes. CSS selectors which you might want to double check: `app-documentation-content`, `.master >` and `.master-content`.

### 20 Sep

- {% badge text="New" type="success" /%} **Embed**: A non-minimal [embed mode](../previewing-documentation.md#embed-mode) is now available.

### 14 Sep

- {% badge text="New" type="success" /%} **Search Analytics**: Enterprise accounts can setup [enterprise search](../using-search/enterprise-search.md) analytics to segment data from different projects.

### 13 Sep

- {% badge text="Security" type="error" /%} **TLS**: All our assets are now served over TLS 1.2 instead of TLS 1.1.

### 10 Sep

- {% badge text="Change" type="warning" /%} **Code Blocks**: Code blocks automatically collapse if it is larger than 100 lines. We also now expand the first line now rather than folding all lines.
- {% badge text="Improvement" /%} **Embed Mode**: Table of contents and index are automatically hidden.

### 08 Sep

- {% badge text="New" type="success" /%} **API Reference**: Can use OpenAPI native variables in Server URL, as well as our own [variables](../variables.md).
- {% badge text="New" type="success" /%} **API**: Two new APIs to [create a page](/api/ref#create-page) and [publish a page](/api/ref#publish-page).

### 07 Sep

- {% badge text="New" type="success" /%} **Page History**: Page history now follows through pages in cloned versions. This means that the creators and contributors will not be lost when a page is cloned, and that you'll be able to access previous versions from the cloned page as well as the original page.

### 06 Sep

- {% badge text="New" type="success" /%} **Page Linking**: After choosing an API reference when page linking, you are now provided with a list of the operations for you to link to directly, rather than having to figure out the URL fragment.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Fix to request bodies with root oneOf/anyOf not showing the table.

### 31 Aug

- {% badge text="New" type="success" /%} **API Reference**: Nested oneOf/anyOf in request body now supported.
- {% badge text="Bug Fix" type="error" /%} **Version Cloning**: Some documentation settings were not cloned to the new documentation when a version is cloned.

### 27 Aug

- {% badge text="New" type="success" /%} **Search Engine**: Setup your docs site as a [search engine](../using-search.md#searching-using-url) on browsers.

### 26 Aug

- {% badge text="New" type="success" /%} **PDF Export**: Enterprise customers can [export an entire version to PDF](../pdf-export.md).

### 20 Aug

- {% badge text="New" type="success" /%} **Page Details**: See page creator from Sidebar \> Page.

### 13 Aug

- {% badge text="Bug Fix" type="error" /%} **Font**: Custom landing pages did not inherit the project font by default.

### 11 Aug

- {% badge text="New" type="success" /%} **Search**: Enabled [advanced search operators](../using-search.md#advanced-search-operators) for our lightning-fast search.
- {% badge text="Bug Fix" type="error" /%} **API References**: No longer show a collapsed table when `requestBody` is defined but empty.

### 10 Aug

- {% badge text="New" type="success" /%} **Read Page API**: Added an [API](/api/ref#read-page) to read pages in [Darkdown](../exporting-documentation.md#darkdown) or text format.
- {% badge text="New" type="success" /%} **Users**: Search through the team members list by name/email.

### 09 Aug

- {% badge text="Bug Fix" type="error" /%} **Page Linking**: Links with specified titles having commas were causing the browser to hang.

### 07 Aug

- {% badge text="New" type="success" /%} **Organisation Search**: Multi project search in a list fashion is available now for Enterprise plans.

### 29 Jul

- {% badge text="New" type="success" /%} **API**: New [API](/api/ref) available to update version which allows you to publish and unpublish a version programmatically.
- {% badge text="New" type="success" /%} **Re-ordering Index**: Re-arrange elements in a big index fast by entering the menu, click Re-arrange, and choosing a category to move it to.

### 26 Jul

- {% badge text="Bug Fix" type="error" /%} **Password Protection**: Minority of customers who set up passwords before 2020 were unable to access anymore using the secure links they previously generated due to deprecation of the old system. The old system has been recovered now.

### 25 Jul

- {% badge text="New" type="success" /%} **JWT authentication**: Use [custom login](../private-docs/custom-login.md) through JWT to log in your readers and [personalise](../personalised-docs.md) their docs.

### 20 Jul

- {% badge text="New" type="success" /%} **Documentation Settings**: You can now only [show the date](../documentation-settings.md#show-page-last-updated) without the author in "Last Page Updated" section at the bottom of the page, without needing to modify CSS.
- {% badge text="New" type="success" /%} **Formatting**: External links will now show a top-right pointing arrow in editor mode to indicate that they are external links, not [internal links](../writing-documentation/page-linking.md).
- {% badge text="Bug Fix" type="error" /%} **Audit**: Deleting version was spamming the audit log with multiple entries.

### 13 Jul

- {% badge text="Bug Fix" type="error" /%} **Search**: Search could fail due to expired search token if a user does not visit the landing page after the search token expires.

### 12 Jul

- {% badge text="New" type="success" /%} **Hosting**: [Host multiple projects](../hosting.md#hosting-multiple-projects-under-one-site) under the same subdomain or custom domain.
- {% badge text="Bug Fix" type="error" /%} **Landing Page**: Clicking on the logo to go to landing page did not change the URL.

### 29 Jun

- {% badge text="Bug Fix" type="error" /%} **Import/Export**: Further fixes to new lines import/export for tables, as well as supporting new lines in table headers when importing.

### 23 Jun

- {% badge text="New" type="success" /%} **Formatting**: Heading 4 is now available through all the different methods of [formatting](../writing-documentation/formatting-text.md).
- {% badge text="New" type="success" /%} **UI Translation**: French is now available as a pre-defined [UI language](../customising-visuals/ui-translation.md).

### 21 Jun

- {% badge text="Bug Fix" type="error" /%} **Import/Export**: Text between tags in tables was not exporting/importing correctly.

### 16 Jun

- {% badge text="New" type="success" /%} **History**: We'll calculate and show you how many lines changed on every change so you know which edits are more signifcant.

### 15 Jun

- {% badge text="Improvement" /%} **Import**: You no longer need to remove HTML tags when importing, we will sanitise it for you.
- {% badge text="Bug Fix" type="error" /%} **Pasting**: Pasting images was not working with Chrome latest update.

### 13 Jun

- {% badge text="New" type="success" /%} **Hosting**: Host your docs in a [subdirectory under your existing website](../hosting.md#hosting-under-an-existing-website).
- {% badge text="New" type="success" /%} **Linked Pages**: View the [pages linking](../writing-documentation/page-linking.md#listing-linked-pages) to any page.

### 22 May

- {% badge text="Security" type="error" /%} **TLS**: Dropped support for the deprecated TLSv1.0 and TLSv1.1.

### 20 May

- {% badge text="New" type="success" /%} **Localisation**: We added a guide for [localisation](../localisation.md).
- {% badge text="New" type="success" /%} **Formatting**: Ordered lists now show different list type so you can reference items better, such as:
  1. This is first item, uses numbering.
     1. This is second item, uses lower alpha.
        1. This is third item, uses lower roman letters.
- {% badge text="New" type="success" /%} **Quick Search**: Option to only search through current version.
- {% badge text="New" type="success" /%} **User Images**: If you sign in with Google, you'll get your profile picture added on DeveloperHub.
- {% badge text="Improvement" /%} **SSO**: If you're an SSO user on Google SAML, then if you click on Sign in using Google, we'll automatically sign you in using SSO.
- {% badge text="Improvement" /%} **Go To**: Go To button now would not add the version slug if you were on the default version.

### 18 May

- {% badge text="New" type="success" /%} **Logout**: When your logged in session expires, you can now log in back without losing what you're working on.
- {% badge text="Security" type="error" /%} **Feedback**: XSS was possible through feedback message input. Feedback messages can no longer have markdown, as it is also a bit of an overkill.

### 17 May

- {% badge text="New" type="success" /%} **SEO**: To disable search engine indexing, you can do it now from Project Settings directly.
- {% badge text="New" type="success" /%} **SEO**: There are now [Advanced Settings](../project-settings/advanced-settings.md) to canonicalise URLs without version slug for the default version, as well as to prevent indexing for older versions.
- {% badge text="Bug Fix" type="error" /%} **Access**: Projects using custom domains were unable to load due to a security rule change. All functionality has been returned to normal now.

### 16 May

- {% badge text="New" type="success" /%} **Images**: You can upload images directly by pasting them.
- {% badge text="New" type="success" /%} **Version Banner**: Added an [advanced setting](../project-settings/advanced-settings.md) to show a banner when the reader is viewing an older version.
- {% badge text="Improvement" /%} **Formatting**: Place cursor correctly after outdenting a list.

### 14 May

- {% badge text="New" type="success" /%} **Formatting**: Nested lists are now supported!
- {% badge text="New" type="success" /%} **Formatting**: Continue numbering for ordered lists (only for first level).

### 9 May

- {% badge text="Change" type="warning" /%} **CSS**: Removed footer default margin.

### 3 May

- {% badge text="New" type="success" /%} **Feedback**: [Feedback](../feedback.md) is now enabled by default for all new projects.
- {% badge text="Bug Fix" type="error" /%} **Links**: Having commas in the title of a link used to break a link.

### 29 Apr

- {% badge text="New" type="success" /%} **Slack Feedback**: [Feedback](../feedback.md) is now sent to [Slack](../integrations/slack.md).

### 25 Apr

- {% badge text="New" type="success" /%} **Feedback**: Gather [feedback](../feedback.md) from your readers right from the pages.
- {% badge text="Change" type="warning" /%} **Search Analytics**: Increase viewable analytics range to 30 days from 14 days.

### 15 Apr

- {% badge text="New" type="success" /%} **Cookie Consent**: Cookie consent text can now be changed.
- {% badge text="Change" type="warning" /%} **API References**: Show "No Scopes" for OAuth2 flows with no scopes, and multiple CSS changes for OAuth2 definitions.

### 12 Apr

- {% badge text="New" type="success" /%} **Open in Editor**: An edit button will be shown at the bottom right of your live docs when you use any of our Go To buttons in the sidebar.

### 10 Apr

- {% badge text="New" type="success" /%} **Require Annotation**: Added a [project setting](../project-settings/advanced-settings.md) to require that editors annotate changes.
- {% badge text="New" type="success" /%} **Open in Editor**: Added a [keyboard shortcut](../keyboard-shortcuts.md) to open pages in editor when in live mode.

### 3 Apr

- {% badge text="New" type="success" /%} **Search Analytics:** Find out how your readers are using search using [Search Analytics](../search-analytics.md).
- {% badge text="New" type="success" /%} **Page Contributors**: Find the list of contributors on a page from Page details menu.
- {% badge text="Bug Fix" type="error" /%} **Index**: Index rarely went out of sync, but no more.

### 1 Apr

- {% badge text="Bug Fix" type="error" /%} **Index**: Drag/drop was too slow for big documentation. Now it is as fast as a one-page documentation!

### 31 Mar

- {% badge text="Improvement" /%} **Import**: Clarify the error when a parent page is expected to exist but does not.

### 29 Mar

- {% badge text="Bug Fix" type="error" /%} **Cloning**: Version cloning was failing if there is an API Reference in the version.

### 28 Mar

- {% badge text="New" type="success" /%} **Lock pages when editing**: Added a project setting to [lock page](../project-settings/advanced-settings.md#lock-page-when-editing) when editing to ensure data does not get overwritten by multiple people editing at the same time.

### 27 Mar

- {% badge text="New" type="success" /%} **User images**: For your user profiles, you can now show your profile photo using [Gravatar](https://gravatar.com/).

### 25 Mar

- {% badge text="Improvement" /%} **Performance**: Loading project for your readers just went 4x faster for smaller projects and 10x faster larger projects 🔥
- {% badge text="New" type="success" /%} **API Reference**: Ability to change the API Reference slug.

### 22 Mar

- {% badge text="New" type="success" /%} **Code Theme**: Use other CodeMirror [code themes](../customising-visuals/code-theme.md).

### 17 Mar

- {% badge text="New" type="success" /%} **Personalise Docs**: Personalise the docs using [injected variables](../variables.md#personalise-docs).
- {% badge text="Improvement" /%} **Editor**: Editor loading is now much faster for users with multiple projects.
- {% badge text="Change" type="warning" /%} **API References**: Disabled breaking words in tables.

### 16 Mar

- {% badge text="New" type="success" /%} **API References**: Added Java OkHttp to [available libraries](../api-references/code-generation.md#available-libraries) for generating example requests.
- {% badge text="New" type="success" /%} **Annotate History**: Add a message to page history to indicate what the change was.

### 10 Mar

- {% badge text="New" type="success" /%} **Image**: Zoom image on click.
- {% badge text="Bug Fix" type="error" /%} **Table Resizing**: Resizing grips were not showing when the column head had formatting.

### 8 Mar

- {% badge text="New" type="success" /%} **Duplicate Index**: Duplicate pages, links, separators and categories right away from the index.
- {% badge text="New" type="success" /%} **CSS**: Added `active-category` class to the currently active category.

### 5 Mar

- {% badge text="New" type="success" /%} **SSO**: [Sign in](../editor-single-sign-on--sso-.md) your users through your Identity Provider (IdP).

### 27 Feb

- {% badge text="Improvement" type="warning" /%} **Cloning**: When cloning a version, if any page had raw HTML, you will now be informed of the page title and documentation title of the offending page.

### 25 Feb

- {% badge text="Bug Fix" type="error" /%} **Editing**: Writing HTML tag-like text in a page no longer can cause unexpected page rendering, such as \<script\>, \<tag\> or else.
- {% badge text="Improvement" type="warning" /%} **General**: You can no longer move from a page with unsaved changes in any way without confirmation

### 22 Feb

- {% badge text="New" type="success" /%} **API References**: Support for generating examples for arrays as well as array items.
- {% badge text="Bug Fix" type="error" /%} **API References**: Description was showing as `default` for requests.

### 20 Feb

- {% badge text="New" type="success" /%} **Tables**: Table columns are now resizable.

### 18 Feb

- {% badge text="New" type="success" /%} **API References**: Added support for `default` in parameters.
- {% badge text="Change" type="warning" /%} **API References**: No longer show headers table if there are no headers.
- {% badge text="Change" type="warning" /%} **API References**: Enhanced design for `enum`  and `default` rendering.
- {% badge text="Bug Fix" type="error" /%} **API References**: Fix to choosing OpenAPI-wide security schemes over operation overrides.
- {% badge text="Bug Fix" type="error" /%} **Index**: When creating a page, the index scroll used to go back to the top.

### 17 Feb

- {% badge text="New" type="success" /%} **API References**: Show request body description for requests, if any.

### 16 Feb

- {% badge text="New" type="success" /%} **API References**: Headers and queries for the selected security scheme now shows in the example request.
- {% badge text="Bug Fix" type="error" /%} **Import**: When an import file has two identical blocks, they used get associated to each other.

### 14 Feb

- {% badge text="Change" type="warning" /%} **CSS**: Font weight for inline code changed to 400 instead of 500. You can revert this change for your project by using `.customise .inline-code{ font-weight: var(--fw-500); }`.

### 9 Feb

- {% badge text="New" type="success" /%} **SEO**: On pasting a documentation link on a social platform/slack/etc..., we'll preview the best image and description of the content possible.
- {% badge text="New" type="success" /%} **API References**: Show response headers under responses.
- {% badge text="New" type="success" /%} **API References**: Added C# HttpClient to [available libraries](../api-references/code-generation.md#available-libraries) for generation request examples.
- {% badge text="New" type="success" /%} **API References CSS**: Add CSS selectors for each field in the tables.

### 8 Feb

- {% badge text="Change" type="warning" /%} **Font**: We have changed the default font to [Nunito](https://fonts.google.com/specimen/Nunito).
- {% badge text="New" type="success" /%} **Font**: Customise [font weights](../customising-visuals/custom-css.md#font-weights) for your font.

### 6 Feb

- {% badge text="New" type="success" /%} **API References**: Allow tags to [expand](../api-references/api-reference-settings.md#allow-tags-to-be-expand).
- {% badge text="New" type="success" /%} **API References**: Show endpoint operations next to tags when expandable.
- {% badge text="New" type="success" /%} **API References**: Show enums for properties.
- {% badge text="New" type="success" /%} **API References**: Tag links in the index are now clickable.
- {% badge text="New" type="success" /%} **API References**: Request and response examples follow scrolling, making it easier for the reader to find the information they need.
- {% badge text="Bug Fix" type="error" /%} **Favicon**: DeveloperHub icon no longer loads by default.
- {% badge text="Change" type="warning" /%} **API References**: CSS makeover, larger titles, more space.

### 4 Feb

- {% badge text="Bug Fix" type="error" /%} **API References**: Fix example request hidden when request body has examples.
- {% badge text="Bug Fix" type="error" /%} **API References**: All Go net/http were showing as GET requests in examples.
- {% badge text="Bug Fix" type="error" /%} **API References**: Response body used to show the array item title as the title of the object.

### 3 Feb

- {% badge text="New" type="success" /%} **API References**: Go net/http and PHP Guzzle are now available as [libraries](../api-references/code-generation.md#available-libraries) for generated request examples.
- {% badge text="New" type="success" /%} **Search**: Search can now be opened using {% key key="⌘" /%}/{% key key="Ctrl" /%} + K for readers.
- {% badge text="Change" type="warning" /%} **Code Generation**: Removed ability to choose which libraries are seen by your users. Majority of API References had all libraries enabled.
- {% badge text="Bug Fix" type="error" /%} **API References**: Request and responses `examples`  included the key `value`. Now it's removed.

### 2 Feb

- {% badge text="New" type="success" /%} **Help \& Support**: New Help \& Support menu to reach our [community discussions](https://talk.developerhub.io), report bugs and submit feature requests.
- {% badge text="New" type="success" /%} **API References**: Requests have support for example under oneOf, anyOf, allOf.
- {% badge text="New" type="success" /%} **API References**: Requests have support for showing the first example of examples.
- {% badge text="New" type="success" /%} **API References**: Responses have support for showing all examples and having them selectable.
- {% badge text="Bug Fix" type="error" /%} **API References**: Requests and responses that have an array of undefined type would show just `array` instead of `array[undefined]`.
- {% badge text="Bug Fix" type="error" /%} **API References**: Requests object title was not shown.
- {% badge text="Bug Fix" type="error" /%} **API References**: Markdown rendering for big images could have overflowed the container.

### 31 Jan

- {% badge text="New" type="success" /%} **Edit History**: [Edit history](../page-history.md) now shows the differences in colours. You can also see the change between current edit and the published edit. Along that, we redesigned a bit the page history panel to focus on published edits rather than drafts.
- {% badge text="Bug Fix" type="error" /%} **Import/Export**: We no longer show import/export options when viewing a page edit history as it was misleading.
- {% badge text="Bug Fix" type="error" /%} **Dashboard**: Comment list was not scrollable if too long.
- {% badge text="Bug Fix" type="error" /%} **Compatibility**: On Safari, project logo width could be miscalculated on same loads causing search bar to fall.

### 27 Jan

- {% badge text="Bug Fix" type="error" /%} **Activity Log**: On reordering indices, there was no icon or good explanation of what happened.
- {% badge text="Bug Fix" type="error" /%} **API References**: Fields other than Operation Objects under Path Item Object used to break an API reference.

### 24 Jan

- {% badge text="New" type="success" /%} **Audit**: Enterprise customers can query [audit logs](../activity-log.md#enterprise-auditing) using the [API](/api/ref#get-activity-log).
- {% badge text="New" type="success" /%} **Get All**: All users can query all resources on %product% using [API](/api/ref#all-project).
- {% badge text="Change" type="warning" /%} **API Rate Limits**: All APIs are rate limited.

### 19 Jan

- {% badge text="New" type="success" /%} **Publishing**: Added a [setting](../project-settings/advanced-settings.md#ask-before-publishing) to prompt you if you are publishing a page that has unresolved comments.
- {% badge text="New" type="success" /%} **Comments**: You can now [resolve](../comments.md#resolve-comments) all comments on a page from the activity bar.
- {% badge text="Improvement" type="warning" /%} **Page Linking**: Search for page linking after typing "@" now searches through titles and slugs. It also tolerates typos.

### 16 Jan

- {% badge text="Bug Fix" type="error" /%} **Blocks**: Duplicating a block more than once at the same time used to have unexpected results.
- {% badge text="Bug Fix" type="error" /%} **Table**: The floating table options control used to float at the wrong place if a row had multiline input.

### 12 Jan

- {% badge text="New" type="success" /%} **Activity Log**: View the latest changes right away from the [dashboard](../collaboration/dashboard.md).
- {% badge text="Improvement" type="warning" /%} **Heading Selection**: When linking a page, we'll automatically copy the heading title if a heading was selected and no title was chosen yet.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: API References were not delete-able from 11 Jan 2021.
- {% badge text="Bug Fix" type="error" /%} **Import**: In case of an incomplete import due to error, we now delete the incomplete versions.

### 11 Jan

- {% badge text="New" type="success" /%} **CSS Changes**: Added a CSS selector to apply CSS to select versions.

### 8 Jan

- {% badge text="New" type="success" /%} **Embed Mode**: Add `?goto=embed` when navigating to a page to enable [embed mode](../previewing-documentation.md#embed-mode).

### 7 Jan

- {% badge text="Change" type="warning" /%} **User Roles**: Publishers can no longer change project colours or top navigation links/icons.
- {% badge text="Bug Fix" type="error" /%} **Colour Picker**: On opening the picker, it used to default colours even if settings were not explicitly changed.
