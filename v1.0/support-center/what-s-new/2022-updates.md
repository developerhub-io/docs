---
type: page
title: 2022 Updates
listed: true
description: 
index_title: 2022 Updates
hidden: false
keywords: 
tags: 
---

### 27 Dec

- {% badge text="Improvement" /%} **API Reference**: Curl requests with `application/octet-stream` media type would show using `--data-binary` instead of `--data` to preserve new lines and carriage in the payload.

### 19 Dec

- {% badge text="Bug Fix" type="error" /%} **Hosting**: Fixed a bug where multi segment base path could cause default page to load instead of the requested page.

### 14 Dec

- {% badge text="Improvement" /%} **Usability**: Enhanced usability of template and synced blocks windows.

### 30 Nov

- {% badge text="Bug Fix" type="error" /%} **API Playground**: Fix for post/put/patch requests with query strings and form data.
- {% badge text="Improvement" /%} **API Playground**: When an API definition doesn't have a server URL, the window location is now used in the example requests.

### 28 Nov

- {% badge text="Bug Fix" type="error" /%} **Dashboard**: Fixed a bug where dashboard no longer loads.

### 27 Nov

- {% badge text="Bug Fix" type="error" /%} **Page Linking**: The page chooser was not always showing in the correct position.

### 22 Nov

- {% badge text="Bug Fix" type="error" /%} **API Reference**: Some API references were failing to get deleted.

### 21 Nov

- {% badge text="New" type="success" /%} **API Editor**: Every API definition edit is now saved in revisions. Edits go into drafts until published.
- {% badge text="Bug Fix" type="error" /%} **API Playground**: Post/Put/Patch requests with query strings were not performed correctly.
- {% badge text="Bug Fix" type="error" /%} **API Playground**: Post/Put/Patch requests with no body were not performed correctly.

### 11 Nov

- {% badge text="Bug Fix" type="error" /%} **Index List**: Index list no longer shows hidden pages too.

### 9 Nov

- {% badge text="New " type="success" /%} **API Editor**: We now have a visual [API Editor](../edit-references.md)!
- {% badge text="Bug Fix" type="error" /%} **API Playground**: Responses for OAS2 weren't showing.

### 5 Nov

- {% badge text="Bug Fix" type="error" /%} **Security**: Links in email invites could have been expired already.

### 27 Oct

- {% badge text="New" type="success" /%} **API Reference**: Basic authentication security scheme now shows username and password fields in the [API Playground](../try-it-out.md) for easier authentication.
- {% badge text="Improvement" /%} **API Reference**: Simplified how Python `requests`  JSON request body show.
- {% badge text="Improvement" /%} **Sidebar**: You can now search for a project rather than having to go through the list.

### 25 Oct

- {% badge text="New" type="success" /%} **API Reference**: We now support uploading OAS 3.1, and listing webhooks 🎉.
- {% badge text="Improvement" /%} **API Reference**: URLs, headers, queries and other pieces of data in cURL requests are now enclosed in single-quotes so they can be copy pasted into a terminal without modification.
- {% badge text="Improvement" /%} **API Reference**: Server/host block is no longer needed when uploading an OpenAPI file.

### 18 Oct

- {% badge text="New" type="success" /%} **GitHub Code**: Embed [code from GitHub](../github-code.md) repository right into %product%.
- {% badge text="New" type="success" /%} **Index List**: Insert a list of [child pages](../index-list.md) dynamically into the page.

### 12 Oct

- {% badge text="Bug Fix" type="error" /%} **Cloning**: When version is cloned, hidden pages in existing version were not hidden anymore in the cloned version.

### 4 Oct

- {% badge text="Bug Fix" type="error" /%} **Image**: Some uploaded images were not showing correctly when zoomed.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Fix to when additionalProperties are showing to be required.

### 25 Sep

- {% badge text="Bug Fix" type="error" /%} **API Reference**: Fix to URL encoding placeholders in example requests/responses.

### 17 Sep

- {% badge text="Improvement" /%} **API Reference**: Tables or examples that are too long get collapsed by default, and can be expanded with a button.
- {% badge text="Improvement" /%} **API Reference**: Code blocks from markdown look like code blocks now.
- {% badge text="Bug Fix " type="error" /%} **API Reference**: Inline code did not have the right font.

### 13 Sep

- {% badge text="New" type="success" /%} **Custom Login**: Ability to generate a [JWT](../private-docs/custom-login.md) token in %product% for easy access.

### 12 Sep

- {% badge text="New" type="success" /%} **API Reference**: Request parameters which have an object type now render correctly in the request table and the examples.
- {% badge text="New" type="success" /%} **API Reference**: Example responses description which have markdown are now rendered in markdown.

### 06 Sep

- {% badge text="New" type="success" /%} **Security**: Ability for projects to be protected by [email invites](../private-docs/email-invite.md).

### 04 Sep

- {% badge text="New" type="success" /%} **API Reference**: [OAuth 2.0 Authentication](../try-it-out.md#oauth-20-authentication) is now possible in Try It Out API Playground.
- {% badge text="New" type="success" /%} **API Reference**: Add support for [Custom Interceptors](../try-it-out.md#custom-interceptors).
- {% badge text="Bug Fix " type="error" /%} **API Reference**: Fixed issue where description might get converted from markdown twice, causing tables to look wrong.

### 25 Aug

- {% badge text="Bug Fix" type="error" /%} **Editor**: Having empty headings could cause content until the previous heading to be deleted.

### 24 Aug

- {% badge text="New" type="success" /%} **API Reference**: Server URL variables are now modifiable in the UI.
- {% badge text="Bug Fix" type="error" /%} **Editor**: Editing an existing page link was broken.

### 18 Aug

- {% badge text="Improvement" /%} **Editor**: {% icon classes="fas fa-plus" /%} sign now shows on new lines even if bold/italic/formatting was applied.
- {% badge text="Bug Fix" type="error" /%} **Editor**: Fix to separators functionality. There was a special case where separator could contain text, which wouldn't be saved.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Inline code in server blocks was not coloured correctly.

### 17 Aug

- {% badge text="New" type="success" /%} **Search Analytics**: Ability to see search analytics for the past 3 or 6 months.
- {% badge text="Bug Fix" type="error" /%} **Editor**: Link selector, inline blocks and other selectors were not showing at the right place inside tabs.

### 14 Aug

- {% badge text="New" type="success" /%} **Tabs**: [Tab blocks](../tabs.md) are now available in beta.
- {% badge text="New" type="success" /%} **Link Analysis**: In addition to showing broken links under page title, we also show unreachable links too. They are all accessible through [link analysis in Page Info](../writing-documentation/page-linking.md#view-broken-links-in-a-page).
- {% badge text="Improvement" /%} **Editor**: Enhancement to how {% key key="Backspace" /%} key works in the editor, ensuring it doesn't delete accidentally more than intended.

### 8 Aug

- {% badge text="Improvement" /%} **Editor**: Documentation index is now collapsible when editing.

### 7 Aug

- {% badge text="New" type="success" /%} **API Reference**: Index can now be set to [collapsible](../api-references/api-reference-settings.md#allow-index-to-collapse).
- {% badge text="Improvement" /%} **Editor**: Improved how the editor handles mixed bold/italic formatting, including overlapping formatting.

### 5 Aug

- {% badge text="Improvement" /%} **Editor**: Disabled {% key key="⇧" /%} + {% key key="↵" /%} completely in the editor. Line breaks use is unusual in technical writing, and they were not supported in any case. Please use the proper elements for providing spaces between content.

### 4 Aug

- {% badge text="New" type="success" /%} **Editor**: Added a guard to ensure you do not close the editor tab when you have unsaved changes.
- {% badge text="Bug Fix" type="error" /%} **Editor**: Fixed some bugs with mixed bold/italic formatting and empty headings.

### 26 Jul

- {% badge text="New" type="success" /%} **Server Headers**: Ability to add custom server [headers](../hosting/server-headers.md) for security purposes.

### 25 Jul

- {% badge text="Improvement" /%} **API Reference**: Objects in request and response tables are bolded now
- {% badge text="Improvement" /%} **API Reference**: Enhanced when example requests and responses stick when scrolling.

### 21 Jul

- {% badge text="New" type="success" /%} **PDF Export**: [API References](../pdf-export.md) are now also exported into the PDF file.

### 19 Jul

- {% badge text="New" type="success" /%} **SEO**: Added [native option](../seo.md#more-custom-options) to disable search engine indexing of non-default version.
- {% badge text="New" type="success" /%} **Import/Export**: API References are now exported and can be imported.
- {% badge text="Improvement" /%} **Table**: Hitting {% key key="Tab" /%} at end of a table will create a new row.

### 15 Jul

- {% badge text="New" type="success" /%} **Custom CSS**: Ability to test on [different frontend application version](../customising-visuals/custom-css.md#testing-css).
- {% badge text="Change" type="warning" /%} **CSS**: Removed `.topnav-container` fixed height and `.mega-container` margin-top. No visual changes.
- {% badge text="Improvement" /%} **Keyboard Shortcuts**: {% key key="⇧" /%} + {% key key="⌥" /%}  + {% key key="D" /%} opens the page in editor if you were on reader site, and the reader site if you were in the editor.

### 14 Jul

{% badge text="cf0aac2" type="custom" /%}

- {% badge text="New" type="success" /%} **URL Redirects**: Added support for [301 server-side URL redirects](../hosting/url-redirects.md).

### 13 Jul

- {% badge text="Improvement" /%} **Customisation**: Custom CSS/Head Tags/Landing Page modals are now resizable to be able to see more code, and you can go to draft mode directly.
- {% badge text="Security" type="error" /%} **Comments**: Resolved a possible XSS issue.

### 12 Jul

- {% badge text="New" type="success" /%} **API Reference**: Added support for `additionalProperties` for request bodies.

### 11 Jul

- {% badge text="Improvement" /%} **API Reference**: We've touched up the API References styles, and it's looking much better!
- {% badge text="New" type="success" /%} **Custom CSS**: You can now [pin frontend application version](../customising-visuals/custom-css.md#pinning-frontend-application-version) when you have heavy CSS changes so our modifications would not affect your readers site.
- {% badge text="Security" type="error" /%} **Hosting**: We now apply `X-Content-Type-Options: nosniff` header to all docs sites to protect against malicious files.
- {% badge text="Change" type="warning" /%} **Editor**: We have tidied up the Project Settings menu.

### 29 Jun

{% badge text="d63b27a" type="custom" /%}

- {% badge text="Change" type="warning" /%} **Code Block**: Rounded code blocks (inside documentation and references) borders.

### 28 Jun

- {% badge text="New" type="success" /%} **Hosting**: Sitemaps for multiple projects hosted by %product% are available now.

### 27 Jun

- {% badge text="Change" type="warning" /%} **Hosting**: Changed the instructions for reverse proxy to include the forwarded request URI. This ensures sitemaps work for multiple projects on the same domain.

### 24 Jun

- {% badge text="New" type="success" /%} **Integrations**: We support Google Analytics 4 IDs for [Google Analytics](../integrations/google-analytics.md) now.

### 23 Jun

- {% badge text="Bug Fix" type="error" /%} **Integrations**: [Google Analytics](../integrations/google-analytics.md) integration might report an out-of-sync page title for a URL.

### 20 Jun

- {% badge text="New" type="success" /%} **Customisations**: Added draft mode to [Custom Landing Page](../landing-page/custom-landing-page.md), [Custom HEAD Tags](../custom-javascript.md) and [Custom CSS](../customising-visuals/custom-css.md) customisations so you can test it before publishing.
- {% badge text="New" type="success" /%} **UI Translation**: HTML lang attribute now changes according to the documentation locale.

### 15 Jun

- {% badge text="New" type="success" /%} **Video**: Can embed [videos](../videos.md#supported-video-platforms) natively from Youtube, Vimeo, Loom and direct URL.

### 11 Jun

- {% badge text="Bug Fix" type="error" /%} **Editor**: Empty headings no longer show as hash characters after saving.
- {% badge text="Bug Fix" type="error" /%} **Editor**: Menu for selecting links and inline variables now opens as expected at start of tables and bullet points.

### 06 Jun

- {% badge text="New" type="success" /%} **Broken Links**: Analyses also internal %product% links which probably should have published docs links.
- {% badge text="New" type="success" /%} **API Reference**: Recognise date-time parameter format.

### 05 Jun

- {% badge text="New" type="success" /%} **API Reference**: Recognise UUID parameter format.
- {% badge text="New" type="success" /%} **API Reference**: Automatic [API Playground](../try-it-out.md) headers and parameters validation. Enums show as options.

### 23 May

- {% badge text="New" type="success" /%} **API Reference**: [API Playground](../try-it-out.md) is now available!

### 15 May

- {% badge text="New" type="success" /%} **PDF Export**: Share a [permalink](../pdf-export.md#pdf-permalink) to allow readers to always download the latest PDF.
- {% badge text="New" type="success" /%} **Custom HTML**: [Custom HTML](../custom-html.md) static contents are now searchable using the search box.
- {% badge text="Bug Fix" type="error" /%} **Private Docs**: URL fragment was not preserved when private docs login showed.

### 12 May

- {% badge text="New" type="success" /%} **Index**: Pages can now be [hidden](../writing-documentation/hidden-pages.md) from index, but still accessible through URL or links.
- {% badge text="Change" type="warning" /%} **Unlisting**: Unlisting is now unpublishing. An unpublished page cannot be viewed by readers.
- {% badge text="Change" type="warning" /%} **PDF Exports**: Any teammate can now download PDFs. Previously it was only publishers and admins.

### 18 Apr

- {% badge text="New" type="success" /%} **API Reference**: Show integer formats if defined in the type column of request and response bodies.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Response user-defined examples may have not shown if there is no authentication scheme.

### 15 Apr

- {% badge text="New" type="success" /%} **API Reference**: Show `additionalProperties` in responses.

### 09 Apr

- {% badge text="Change" type="warning" /%} **Documentation/API Reference**: Creating a new documentation/API reference orders it last. System used to order it first.
- {% badge text="Bug Fix" type="error" /%} **Documentation/API Reference**: Ordering documentation/API reference could have failed previously due to being out of sync. This is now mitigated and ordering is ensured.
- {% badge text="Bug Fix" type="error" /%} **Index**: Ordering a category to the bottom of the index may have merged pages of two categories in an unexpected way. This is now mitigated and ordering is ensured.

### 06 Apr

- {% badge text="New" type="success" /%} **API Reference**: Support for `externalDocs` under schema object.
- {% badge text="New" type="success" /%} **Tables**: Added minimal support for copy/pasting table rows.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Response body table showed `no response body` if there was no schema but headers existed.

### 31 Mar

- {% badge text="New" type="success" /%} **SEO**: Ability to manually specify page description for SEO search engines.

### 28 Mar

- {% badge text="Bug Fix" type="error" /%} **Index**: `categoryToggle` advanced setting also prevented parent page indices from auto-collapsing.

### 18 Mar

- {% badge text="Bug Fix" type="error" /%} **Page Linking**: Clicking on a page link inside a table when in the editor was not showing the window to change the details.
- {% badge text="Bug Fix" type="error" /%} **Index**: Edit Title was not showing the page title by default, and had a misleading button label.

### 16 Mar

- {% badge text="New" type="success" /%} **Code Block**: Add `Groovy` as a language.
- {% badge text="Bug Fix" type="error" /%} **Import**: Importing pages with images hosted by us was showing an error.

### 14 Mar

- {% badge text="Bug Fix" type="error" /%} **API Reference**: Request bodies having no content may not look good. Response body having content with no media type map may not look good.

### 10 Mar

- {% badge text="New" type="success" /%} **API Reference**: Support for `servers` under operation object. If there are servers defined, the first one will be used for the example request server URL.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Dashes in tag titles were getting stripped.
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Responses with `text/html` media types were not rendered correctly.

### 06 Mar

- {% badge text="New" type="success" /%} **API Reference**: Support for multiple security schemes for API or operation security.
- {% badge text="New" type="success" /%} **Custom Login**: [Redirect to a URL](../private-docs/custom-login.md#handling-jwt-login-error) on authentication error.

### 05 Mar

- {% badge text="New" type="success" /%} **CSS**: Added `--brand-active` CSS variable for brand colour over light controls.
- {% badge text="New" type="success" /%} **API Reference**: Rendered markdown tables from descriptions now look like pretty like our tables.
- {% badge text="Change" type="warning" /%} **API Reference**: Rendered markdown separators from descriptions now have margins.

### 01 Mar

- {% badge text="New" type="success" /%} **Teammates**: Admins can now change a teammate's name.
- {% badge text="New" type="success" /%} **Teammates**: Owner can [transfer project ownership](../collaboration.md#changing-project-ownership) without needing to open a support ticket.

### 28 Feb

- {% badge text="Change" type="warning" /%} **Images**: All images are now served through our own AWS Cloudfront distribution and saved in our S3 buckets.

### 19 Feb

- {% badge text="New" type="success" /%} **API Reference**: Show API Reference description headings in the index.
- {% badge text="New" type="success" /%} **Index**: Allow use of variables in external links.

### 06 Feb

- {% badge text="New" type="success" /%} **API Reference**: Option to show [accept header](../api-references/api-reference-settings.md#show-accept-header).
- {% badge text="Bug Fix" type="error" /%} **API Reference**: Authentication header might not show if reference is set to expand tags.

### 31 Jan

- {% badge text="Change" type="warning" /%} **API Reference**: If a schema has no `type`, we'll show faded `<type>` in the table.

### 28 Jan

- {% badge text="Change" type="warning" /%} **Index**: We now show a warning when you are trying to create a page when a page is not saved yet.
- {% badge text="Bug Fix" type="error" /%} **Separator**: You can now click down or enter to continue writing below the last separator on the page.

### 27 Jan

- {% badge text="New" type="success" /%} **Page Linking**: Instead of removing link all together, you can now click on a link to modify its label and linked heading.
- {% badge text="Change" type="warning" /%} **Version**: Version now gets unpublished automatically if all sections below it are unpublished. You also cannot publish a version anymore which has unpublished sections.
- {% badge text="Bug Fix" type="error" /%} **Index**: Re-arrange page menu might get hidden if category titles were too long and screen size was small.

### 24 Jan

- {% badge text="Bug Fix" type="error" /%} **Index**: Drag and drop is much faster now when using a trackpad.

### 17 Jan

- {% badge text="New" type="success" /%} **Index**: [Rename index title](../structuring-documentation/managing-pages.md#renaming-page-index) without renaming the page.

### 12 Jan

- {% badge text="New" type="success" /%} **Documentation**: You can now control publishing state for documentation sections.
- {% badge text="New" type="success" /%} **API Reference**: You can now control publishing state for API reference sections.
- {% badge text="Change" type="warning" /%} **Editor Layout**: All version, documentation and API reference settings are now available under a Settings {% icon classes="fas fa-cog" /%} menu to declutter the menus.
- {% badge text="Change" type="warning" /%} **Page Info**: Page {% icon classes="fas fa-file-alt" /%} has moved from the left sidebar to the right sidebar under Page Info.
- {% badge text="Change" type="warning" /%} **Documentation**: All documentation that already existed with no listed pages became unpublished. You can no longer have a documentation that is published without any listed pages under it.

### 07 Jan

- {% badge text="Bug Fix" type="error" /%} **Tables**: Fixed an issue where creating two columns consecutively would add them in the wrong order.
- {% badge text="Bug Fix" type="error" /%} **Tables**: Keyboard cursor was not in the right place for empty headers.

### 04 Jan

- {% badge text="New" type="success" /%} **Users**: Ability to [deprovision](../editor-single-sign-on--sso-.md#deprovisioning-users) teammates from a managed organisation.
- {% badge text="New" type="success" /%} **Feedback**: Revamped how feedback inbox looks and page feedback. You now see all feedback without having to toggle between read and unread. Also, feedback without messages also show in the inbox. Moreover, you can click on the chart above feedback inbox to look at the feedback for that day.
