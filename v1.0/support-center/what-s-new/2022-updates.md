---
type: page
title: 2022 Updates
listed: true
slug: 2022-updates
description: 
index_title: 2022 Updates
hidden: 
keywords: 
tags: 
---

### 27 Dec

- {% badge type="info" text="Improvement" /%} **API Reference**: Curl requests with `application/octet-stream` media type would show using `--data-binary` instead of `--data` to preserve new lines and carriage in the payload.

### 19 Dec

- {% badge type="error" text="Bug Fix" /%} **Hosting**: Fixed a bug where multi segment base path could cause default page to load instead of the requested page.

### 14 Dec

- {% badge type="info" text="Improvement" /%} **Usability**: Enhanced usability of template and synced blocks windows.

### 30 Nov

- {% badge type="error" text="Bug Fix" /%} **API Playground**: Fix for post/put/patch requests with query strings and form data.
- {% badge type="info" text="Improvement" /%} **API Playground**: When an API definition doesn't have a server URL, the window location is now used in the example requests.

### 28 Nov

- {% badge type="error" text="Bug Fix" /%} **Dashboard**: Fixed a bug where dashboard no longer loads.

### 27 Nov

- {% badge type="error" text="Bug Fix" /%} **Page Linking**: The page chooser was not always showing in the correct position.

### 22 Nov

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Some API references were failing to get deleted.

### 21 Nov

- {% badge type="success" text="New" /%} **API Editor**: Every API definition edit is now saved in revisions. Edits go into drafts until published.
- {% badge type="error" text="Bug Fix" /%} **API Playground**: Post/Put/Patch requests with query strings were not performed correctly.
- {% badge type="error" text="Bug Fix" /%} **API Playground**: Post/Put/Patch requests with no body were not performed correctly.

### 11 Nov

- {% badge type="error" text="Bug Fix" /%} **Index List**: Index list no longer shows hidden pages too.

### 9 Nov

- {% badge type="success" text="New " /%} **API Editor**: We now have a visual [API Editor](/support-center/edit-references)!
- {% badge type="error" text="Bug Fix" /%} **API Playground**: Responses for OAS2 weren't showing.

### 5 Nov

- {% badge type="error" text="Bug Fix" /%} **Security**: Links in email invites could have been expired already.

### 27 Oct

- {% badge type="success" text="New" /%} **API Reference**: Basic authentication security scheme now shows username and password fields in the [API Playground](/support-center/try-it-out) for easier authentication.
- {% badge type="info" text="Improvement" /%} **API Reference**: Simplified how Python `requests`  JSON request body show.
- {% badge type="info" text="Improvement" /%} **Sidebar**: You can now search for a project rather than having to go through the list.

### 25 Oct

- {% badge type="success" text="New" /%} **API Reference**: We now support uploading OAS 3.1, and listing webhooks 🎉.
- {% badge type="info" text="Improvement" /%} **API Reference**: URLs, headers, queries and other pieces of data in cURL requests are now enclosed in single-quotes so they can be copy pasted into a terminal without modification.
- {% badge type="info" text="Improvement" /%} **API Reference**: Server/host block is no longer needed when uploading an OpenAPI file.

### 18 Oct

- {% badge type="success" text="New" /%} **GitHub Code**: Embed [code from GitHub](/support-center/github-code) repository right into %product%.
- {% badge type="success" text="New" /%} **Index List**: Insert a list of [child pages](/support-center/index-list) dynamically into the page.

### 12 Oct

- {% badge type="error" text="Bug Fix" /%} **Cloning**: When version is cloned, hidden pages in existing version were not hidden anymore in the cloned version.

### 4 Oct

- {% badge type="error" text="Bug Fix" /%} **Image**: Some uploaded images were not showing correctly when zoomed.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Fix to when additionalProperties are showing to be required.

### 25 Sep

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Fix to URL encoding placeholders in example requests/responses.

### 17 Sep

- {% badge type="info" text="Improvement" /%} **API Reference**: Tables or examples that are too long get collapsed by default, and can be expanded with a button.
- {% badge type="info" text="Improvement" /%} **API Reference**: Code blocks from markdown look like code blocks now.
- {% badge type="error" text="Bug Fix " /%} **API Reference**: Inline code did not have the right font.

### 13 Sep

- {% badge type="success" text="New" /%} **Custom Login**: Ability to generate a [JWT](/support-center/custom-login) token in %product% for easy access.

### 12 Sep

- {% badge type="success" text="New" /%} **API Reference**: Request parameters which have an object type now render correctly in the request table and the examples.
- {% badge type="success" text="New" /%} **API Reference**: Example responses description which have markdown are now rendered in markdown.

### 06 Sep

- {% badge type="success" text="New" /%} **Security**: Ability for projects to be protected by [email invites](/support-center/email-invite).

### 04 Sep

- {% badge type="success" text="New" /%} **API Reference**: [OAuth 2.0 Authentication](/support-center/try-it-out#oauth-20-authentication) is now possible in Try It Out API Playground.
- {% badge type="success" text="New" /%} **API Reference**: Add support for [Custom Interceptors](/support-center/try-it-out#custom-interceptors).
- {% badge type="error" text="Bug Fix " /%} **API Reference**: Fixed issue where description might get converted from markdown twice, causing tables to look wrong.

### 25 Aug

- {% badge type="error" text="Bug Fix" /%} **Editor**: Having empty headings could cause content until the previous heading to be deleted.

### 24 Aug

- {% badge type="success" text="New" /%} **API Reference**: Server URL variables are now modifiable in the UI.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Editing an existing page link was broken.

### 18 Aug

- {% badge type="info" text="Improvement" /%} **Editor**: {% icon classes="fas fa-plus" /%} sign now shows on new lines even if bold/italic/formatting was applied.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Fix to separators functionality. There was a special case where separator could contain text, which wouldn't be saved.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Inline code in server blocks was not coloured correctly.

### 17 Aug

- {% badge type="success" text="New" /%} **Search Analytics**: Ability to see search analytics for the past 3 or 6 months.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Link selector, inline blocks and other selectors were not showing at the right place inside tabs.

### 14 Aug

- {% badge type="success" text="New" /%} **Tabs**: [Tab blocks](/support-center/tabs) are now available in beta.
- {% badge type="success" text="New" /%} **Link Analysis**: In addition to showing broken links under page title, we also show unreachable links too. They are all accessible through [link analysis in Page Info](/support-center/page-linking#view-broken-links-in-a-page).
- {% badge type="info" text="Improvement" /%} **Editor**: Enhancement to how {% key key="Backspace" /%} key works in the editor, ensuring it doesn't delete accidentally more than intended.

### 8 Aug

- {% badge type="info" text="Improvement" /%} **Editor**: Documentation index is now collapsible when editing.

### 7 Aug

- {% badge type="success" text="New" /%} **API Reference**: Index can now be set to [collapsible](/support-center/api-reference-settings#allow-index-to-collapse).
- {% badge type="info" text="Improvement" /%} **Editor**: Improved how the editor handles mixed bold/italic formatting, including overlapping formatting.

### 5 Aug

- {% badge type="info" text="Improvement" /%} **Editor**: Disabled {% key key="⇧" /%} + {% key key="↵" /%} completely in the editor. Line breaks use is unusual in technical writing, and they were not supported in any case. Please use the proper elements for providing spaces between content.

### 4 Aug

- {% badge type="success" text="New" /%} **Editor**: Added a guard to ensure you do not close the editor tab when you have unsaved changes.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Fixed some bugs with mixed bold/italic formatting and empty headings.

### 26 Jul

- {% badge type="success" text="New" /%} **Server Headers**: Ability to add custom server [headers](/support-center/server-headers) for security purposes.

### 25 Jul

- {% badge type="info" text="Improvement" /%} **API Reference**: Objects in request and response tables are bolded now
- {% badge type="info" text="Improvement" /%} **API Reference**: Enhanced when example requests and responses stick when scrolling.

### 21 Jul

- {% badge type="success" text="New" /%} **PDF Export**: [API References](/support-center/pdf-export) are now also exported into the PDF file.

### 19 Jul

- {% badge type="success" text="New" /%} **SEO**: Added [native option](/support-center/seo#more-custom-options) to disable search engine indexing of non-default version.
- {% badge type="success" text="New" /%} **Import/Export**: API References are now exported and can be imported.
- {% badge type="info" text="Improvement" /%} **Table**: Hitting {% key key="Tab" /%} at end of a table will create a new row.

### 15 Jul

- {% badge type="success" text="New" /%} **Custom CSS**: Ability to test on [different frontend application version](/support-center/custom-css#testing-css).
- {% badge type="warning" text="Change" /%} **CSS**: Removed `.topnav-container` fixed height and `.mega-container` margin-top. No visual changes.
- {% badge type="info" text="Improvement" /%} **Keyboard Shortcuts**: {% key key="⇧" /%} + {% key key="⌥" /%}  + {% key key="D" /%} opens the page in editor if you were on reader site, and the reader site if you were in the editor.

### 14 Jul

{% badge type="custom" text="cf0aac2" /%}

- {% badge type="success" text="New" /%} **URL Redirects**: Added support for [301 server-side URL redirects](/support-center/url-redirects).

### 13 Jul

- {% badge type="info" text="Improvement" /%} **Customisation**: Custom CSS/Head Tags/Landing Page modals are now resizable to be able to see more code, and you can go to draft mode directly.
- {% badge type="error" text="Security" /%} **Comments**: Resolved a possible XSS issue.

### 12 Jul

- {% badge type="success" text="New" /%} **API Reference**: Added support for `additionalProperties` for request bodies.

### 11 Jul

- {% badge type="info" text="Improvement" /%} **API Reference**: We've touched up the API References styles, and it's looking much better!
- {% badge type="success" text="New" /%} **Custom CSS**: You can now [pin frontend application version](/support-center/custom-css#pinning-frontend-application-version) when you have heavy CSS changes so our modifications would not affect your readers site.
- {% badge type="error" text="Security" /%} **Hosting**: We now apply `X-Content-Type-Options: nosniff` header to all docs sites to protect against malicious files.
- {% badge type="warning" text="Change" /%} **Editor**: We have tidied up the Project Settings menu.

### 29 Jun

{% badge type="custom" text="d63b27a" /%}

- {% badge type="warning" text="Change" /%} **Code Block**: Rounded code blocks (inside documentation and references) borders.

### 28 Jun

- {% badge type="success" text="New" /%} **Hosting**: Sitemaps for multiple projects hosted by %product% are available now.

### 27 Jun

- {% badge type="warning" text="Change" /%} **Hosting**: Changed the instructions for reverse proxy to include the forwarded request URI. This ensures sitemaps work for multiple projects on the same domain.

### 24 Jun

- {% badge type="success" text="New" /%} **Integrations**: We support Google Analytics 4 IDs for [auto$](/support-center/google-analytics) now.

### 23 Jun

- {% badge type="error" text="Bug Fix" /%} **Integrations**: [auto$](/support-center/google-analytics) integration might report an out-of-sync page title for a URL.

### 20 Jun

- {% badge type="success" text="New" /%} **Customisations**: Added draft mode to [auto$](/support-center/custom-landing-page), [auto$](/support-center/custom-javascript) and [auto$](/support-center/custom-css) customisations so you can test it before publishing.
- {% badge type="success" text="New" /%} **UI Translation**: HTML lang attribute now changes according to the documentation locale.

### 15 Jun

- {% badge type="success" text="New" /%} **Video**: Can embed [videos](/support-center/videos#supported-video-platforms) natively from Youtube, Vimeo, Loom and direct URL.

### 11 Jun

- {% badge type="error" text="Bug Fix" /%} **Editor**: Empty headings no longer show as hash characters after saving.
- {% badge type="error" text="Bug Fix" /%} **Editor**: Menu for selecting links and inline variables now opens as expected at start of tables and bullet points.

### 06 Jun

- {% badge type="success" text="New" /%} **Broken Links**: Analyses also internal %product% links which probably should have published docs links.
- {% badge type="success" text="New" /%} **API Reference**: Recognise date-time parameter format.

### 05 Jun

- {% badge type="success" text="New" /%} **API Reference**: Recognise UUID parameter format.
- {% badge type="success" text="New" /%} **API Reference**: Automatic [auto$](/support-center/try-it-out) headers and parameters validation. Enums show as options.

### 23 May

- {% badge type="success" text="New" /%} **API Reference**: [auto$](/support-center/try-it-out) is now available!

### 15 May

- {% badge type="success" text="New" /%} **PDF Export**: Share a [permalink](/support-center/pdf-export#pdf-permalink) to allow readers to always download the latest PDF.
- {% badge type="success" text="New" /%} **Custom HTML**: [Custom HTML](/support-center/custom-html) static contents are now searchable using the search box.
- {% badge type="error" text="Bug Fix" /%} **Private Docs**: URL fragment was not preserved when private docs login showed.

### 12 May

- {% badge type="success" text="New" /%} **Index**: Pages can now be [hidden](/support-center/hidden-pages) from index, but still accessible through URL or links.
- {% badge type="warning" text="Change" /%} **Unlisting**: Unlisting is now unpublishing. An unpublished page cannot be viewed by readers.
- {% badge type="warning" text="Change" /%} **PDF Exports**: Any teammate can now download PDFs. Previously it was only publishers and admins.

### 18 Apr

- {% badge type="success" text="New" /%} **API Reference**: Show integer formats if defined in the type column of request and response bodies.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Response user-defined examples may have not shown if there is no authentication scheme.

### 15 Apr

- {% badge type="success" text="New" /%} **API Reference**: Show `additionalProperties` in responses.

### 09 Apr

- {% badge type="warning" text="Change" /%} **Documentation/API Reference**: Creating a new documentation/API reference orders it last. System used to order it first.
- {% badge type="error" text="Bug Fix" /%} **Documentation/API Reference**: Ordering documentation/API reference could have failed previously due to being out of sync. This is now mitigated and ordering is ensured.
- {% badge type="error" text="Bug Fix" /%} **Index**: Ordering a category to the bottom of the index may have merged pages of two categories in an unexpected way. This is now mitigated and ordering is ensured.

### 06 Apr

- {% badge type="success" text="New" /%} **API Reference**: Support for `externalDocs` under schema object.
- {% badge type="success" text="New" /%} **Tables**: Added minimal support for copy/pasting table rows.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Response body table showed `no response body` if there was no schema but headers existed.

### 31 Mar

- {% badge type="success" text="New" /%} **SEO**: Ability to manually specify page description for SEO search engines.

### 28 Mar

- {% badge type="error" text="Bug Fix" /%} **Index**: `categoryToggle` advanced setting also prevented parent page indices from auto-collapsing.

### 18 Mar

- {% badge type="error" text="Bug Fix" /%} **Page Linking**: Clicking on a page link inside a table when in the editor was not showing the window to change the details.
- {% badge type="error" text="Bug Fix" /%} **Index**: Edit Title was not showing the page title by default, and had a misleading button label.

### 16 Mar

- {% badge type="success" text="New" /%} **Code Block**: Add `Groovy` as a language.
- {% badge type="error" text="Bug Fix" /%} **Import**: Importing pages with images hosted by us was showing an error.

### 14 Mar

- {% badge type="error" text="Bug Fix" /%} **API Reference**: Request bodies having no content may not look good. Response body having content with no media type map may not look good.

### 10 Mar

- {% badge type="success" text="New" /%} **API Reference**: Support for `servers` under operation object. If there are servers defined, the first one will be used for the example request server URL.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Dashes in tag titles were getting stripped.
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Responses with `text/html` media types were not rendered correctly.

### 06 Mar

- {% badge type="success" text="New" /%} **API Reference**: Support for multiple security schemes for API or operation security.
- {% badge type="success" text="New" /%} **Custom Login**: [Redirect to a URL](/support-center/custom-login#handling-jwt-login-error) on authentication error.

### 05 Mar

- {% badge type="success" text="New" /%} **CSS**: Added `--brand-active` CSS variable for brand colour over light controls.
- {% badge type="success" text="New" /%} **API Reference**: Rendered markdown tables from descriptions now look like pretty like our tables.
- {% badge type="warning" text="Change" /%} **API Reference**: Rendered markdown separators from descriptions now have margins.

### 01 Mar

- {% badge type="success" text="New" /%} **Teammates**: Admins can now change a teammate's name.
- {% badge type="success" text="New" /%} **Teammates**: Owner can [transfer project ownership](/support-center/collaboration#changing-project-ownership) without needing to open a support ticket.

### 28 Feb

- {% badge type="warning" text="Change" /%} **Images**: All images are now served through our own AWS Cloudfront distribution and saved in our S3 buckets.

### 19 Feb

- {% badge type="success" text="New" /%} **API Reference**: Show API Reference description headings in the index.
- {% badge type="success" text="New" /%} **Index**: Allow use of variables in external links.

### 06 Feb

- {% badge type="success" text="New" /%} **API Reference**: Option to show [accept header](/support-center/api-reference-settings#show-accept-header).
- {% badge type="error" text="Bug Fix" /%} **API Reference**: Authentication header might not show if reference is set to expand tags.

### 31 Jan

- {% badge type="warning" text="Change" /%} **API Reference**: If a schema has no `type`, we'll show faded `<type>` in the table.

### 28 Jan

- {% badge type="warning" text="Change" /%} **Index**: We now show a warning when you are trying to create a page when a page is not saved yet.
- {% badge type="error" text="Bug Fix" /%} **Separator**: You can now click down or enter to continue writing below the last separator on the page.

### 27 Jan

- {% badge type="success" text="New" /%} **Page Linking**: Instead of removing link all together, you can now click on a link to modify its label and linked heading.
- {% badge type="warning" text="Change" /%} **Version**: Version now gets unpublished automatically if all sections below it are unpublished. You also cannot publish a version anymore which has unpublished sections.
- {% badge type="error" text="Bug Fix" /%} **Index**: Re-arrange page menu might get hidden if category titles were too long and screen size was small.

### 24 Jan

- {% badge type="error" text="Bug Fix" /%} **Index**: Drag and drop is much faster now when using a trackpad.

### 17 Jan

- {% badge type="success" text="New" /%} **Index**: [Rename index title](/support-center/managing-pages#renaming-page-index) without renaming the page.

### 12 Jan

- {% badge type="success" text="New" /%} **Documentation**: You can now control publishing state for documentation sections.
- {% badge type="success" text="New" /%} **API Reference**: You can now control publishing state for API reference sections.
- {% badge type="warning" text="Change" /%} **Editor Layout**: All version, documentation and API reference settings are now available under a Settings {% icon classes="fas fa-cog" /%} menu to declutter the menus.
- {% badge type="warning" text="Change" /%} **Page Info**: Page {% icon classes="fas fa-file-alt" /%} has moved from the left sidebar to the right sidebar under Page Info.
- {% badge type="warning" text="Change" /%} **Documentation**: All documentation that already existed with no listed pages became unpublished. You can no longer have a documentation that is published without any listed pages under it.

### 07 Jan

- {% badge type="error" text="Bug Fix" /%} **Tables**: Fixed an issue where creating two columns consecutively would add them in the wrong order.
- {% badge type="error" text="Bug Fix" /%} **Tables**: Keyboard cursor was not in the right place for empty headers.

### 04 Jan

- {% badge type="success" text="New" /%} **Users**: Ability to [deprovision](/support-center/editor-single-sign-on--sso-#deprovisioning-users) teammates from a managed organisation.
- {% badge type="success" text="New" /%} **Feedback**: Revamped how feedback inbox looks and page feedback. You now see all feedback without having to toggle between read and unread. Also, feedback without messages also show in the inbox. Moreover, you can click on the chart above feedback inbox to look at the feedback for that day.
