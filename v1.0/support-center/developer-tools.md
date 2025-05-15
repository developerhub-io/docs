---
type: page
title: Developer Tools
listed: true
slug: developer-tools
description: 
index_title: Developer Tools
hidden: 
keywords: 
tags: customisation
---

%product% functionality can be modified, accessed and tested in many ways:

- Adding query params to the URL.
- Using javascript functions.
- Using scripts that listen to javascript events triggered.
- Using scripts that modify settings.
- Reading javascript objects.

## URL Modifications

### Embed Mode

Query: `?mode=<mode>`

Strips away top navigation, index, table of contents, footer and others for preview mode. See [Embed Mode](/support-center/previewing-documentation#embed-mode).

### Disable Scripts

Query: `?disableScripts=true`

Disables scripts momentarily. See [Disabling HEAD Tags](/support-center/custom-javascript#disabling-head-tags).

### Disable Styles

Query: `?disableStyles=true`

Disables styles momentarily. See [Disabling Styles](/support-center/custom-css#disabling-styles).

### Personalisation - Clear Text

Query: `?vars=<vars>`

Personalises the documentation by overriding variables with clear text in JSON format. See [Personalising through URL](/support-center/personalised-docs#personalising-through-url).

### Personalisation - Base64

Query: `?hvars=<vars>`

Personalises the documentation by overriding variables with base64 text. See [Personalising through URL](/support-center/personalised-docs#personalising-through-url).

### JWT Authentication

Query: `?jwt=<token>`

Securely give access to the docs. See [auto$](/support-center/custom-login).

### Set Frontend Application Deployment ID

Query: `?deployment_id=<id>` 

Sets the frontend application deployment version. Use `latest` for latest version. See [Testing CSS](/support-center/custom-css#testing-css).

## Javascript Functions

### Navigate to URL (Deprecated)

Function: `openLink(event, link)`

Returns: Nothing.

Arguments:

- `event`: the MouseEvent or KeyboardEvent.
- `link`: Absolute path (without host and basepath) such as `/support-center/developer-tools`.

See [Linking to Content](/support-center/custom-landing-page#linking-to-content).

Deprecated: Use [Navigate to Path](/support-center/developer-tools#navigate-to-path) instead.

### Navigate to Path

Function: `navigate(link, options ?: {addBasePath: boolean})` 

Returns: Nothing.

Arguments:

- `link`: Absolute path (without host and basepath) such as `/support-center/developer-tools`.
- `options`: (optional)
    - `addBasePath`: Prepends the base path automatically to the link.

Navigates to a path internally inside the single page application, without reloading the page. See [Linking to Content](/support-center/custom-landing-page#linking-to-content).

### Navigate Home

Function `goHome()` 

Returns: Nothing.

Arguments: None.

Goes to landing page, or to the default page if no landing page is set. Equivalent to `openLink('/')` when the project has no basepath.

### Make All Landing Page Links Route in SPA

Function: `window.applyClickHandlersOnLinks()` 

Returns: Nothing.

Arguments: None.

Captures all absolute paths on a rendered landing page and routes them internally in the single-page application rather than a browser tab navigation. Use after all anchor elements have been rendered on a landing page. See [Custom Landing Page](/support-center/custom-landing-page#adding-javascript).

### Resize Custom HTML iFrame

Function: `window.postMessage('resize', '*');`

Returns: Nothing.

Arguments: Must be provided as is.

Informs the parent element to resize because elements have been dynamically added to the iFrame. See [Resizing Dynamic iFrames](/support-center/custom-html#resizing-dynamic-iframes).

### Apply Advanced Settings

Function: `window.settings.apply(settings)`

Returns: Nothing.

Arguments:

- `settings`: An object containing [specific settings](/support-center/advanced-settings#applying-settings).

Modifies UI or functionality, including search, code theme, SEO and others. See [Applying Settings](/support-center/advanced-settings#applying-settings).

### Modify UI Text

Function: `window.translations.apply(translation)`

Returns: Nothing.

Arguments:

- `translation`: An object containing [certain UI texts that can be changed](/support-center/ui-translation#which-text-can-be-changed).

Modifies UI text, whether for translation or else. See [auto$](/support-center/ui-translation).

### Register Custom Interceptors

Function: `window.registerCustomInterceptor(interceptor)` 

Returns: Nothing.

Arguments:

- `interceptor`: A function with two arguments, `data` and `next`. See [Custom Interceptors](/support-center/try-it-out#how-to-set-up-custom-interceptors).

Registers a custom interceptor that can modify API playground requests before they're sent.

### Get Active Project

Function: `window.getActiveProject()` 

Returns: `Project Object {id: number, title: string, slug: string, basepath: string}`

### Get Active Version

Function: `window.getActiveVersion()` 

Returns: `Version Object {id: number, name: string, slug: string, docs: {id: number, title: string, slug: string}[], refs: {id: number, title: string, slug: string}[]}` or `null`

### Get Active Section

Function: `window.getActiveSection()` 

Returns: `Section Object {id: number, title: string, slug: string, type: string, index: any}` or `null`

### Get Active Page

Function: `window.getActivePage()` 

Returns: `Page Object {id: number, title: string, slug: string}` or `null`

### Zoom Image

Function: `window.zoomImage(src)`

Return: Nothing.

Arguments:

- `src`: The URL of the image to load.

Loads the image in an overlay over the docs, just like when native images are clicked on product.

### Zoom Image from within an iFrame

Function: `window.postMessage({zoomImage: src}, '*')`

Return: Nothing.

Arguments:

- `src`: The URL of the image to load.

Loads the image in an overlay over the docs, just like when native images are clicked on product. Use it when the image is created by a [auto$](/support-center/custom-html) which uses an iFrame (when there is a script or iFrame).

### Change Theme

Function: `window.setTheme(theme: 'light' | 'dark')` 

Return: Nothing.

Arguments:

- `theme`: Either `light` or `dark`.

Changes the theme for the session.

## Javascript Dispatched Events

### Landing Page Cards Generated

Event: `oncardschanged`

When: Landing page is loading

Emits: Details about every documentation and API reference in the default version which make up the cards in the landing page. See [Adding Javascript](/support-center/custom-landing-page#adding-javascript).

### On Project Loaded

Event: `onprojectloaded`

When: Project has loaded. DOM elements should already be available now for manipulation if needed.

Emits: Nothing. See [Project Loaded](/support-center/custom-javascript#project-loaded).

### On Version Change

Event: `onversionchange`

When: When version has changed.

Emits: Details about the version that is being switched to.

### On Section Change

Event: `onsectionchange`

When: When section (documentation or API reference) is changing.

Emits: Details about the section that is being switched to. See [Section Changes](/support-center/custom-javascript#section-changes).

### On Page Change

Event: `onpagechange`

When: When page is changing.

Emits: Details about the page that is being switched to. See [Page Changes](/support-center/custom-javascript#page-changes).

### On Page Loaded

Event: `onpageloaded`

When: When page has loaded.

Emits: Details about the page that has loaded. Note that async-retrieved objects may not have loaded yet, such as images or videos.

### On Reference Content Loaded

Event: `onreferencecontentloaded` 

When: When reference has loaded and UI is ready. Also when a tag expands and shows new content.

Emits: The HTML element that loaded if you wish to make customisations to the API reference UI, as follows:

{% code %}
{% tab language="json" %}
{
  el: HTMLElement
}
{% /tab %}
{% /code %}

### On Search

Event: `onsearch` 

When: When search has been performed.

Emits: Details about the query and hits count as follows:

{% code %}
{% tab language="json" %}
{
  query: string,
  hitsCount: number,
  type: 'normal'|'ai'
}
{% /tab %}
{% /code %}

{% callout type="warning" title="Only Non-Enterprise Search" %}
This is only available for non-enterprise search currently.
{% /callout %}

### On Feedback

Event: `onfeedback`

When: When feedback (like/dislike) vote has been registered.

Emits: Details about the feedback as follows:

{% code %}
{% tab language="json" %}
{
  action: 'vote',
  vote: boolean, // true for like, false for dislike
  pageUrl: string
}
{% /tab %}
{% /code %}

## Javascript Objects

### Accessing Variables

Object: `window.vars`

Access current variables set in the documentation. Available after the project loads. See [Using Project Variables in Scripts](/support-center/variables#using-project-variables-in-scripts).