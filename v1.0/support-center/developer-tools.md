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

%product% functionality can be modified, accessed, and tested through URL query parameters, JavaScript functions, dispatched events, and global objects.

- Adding query params to the URL.
- Using javascript functions.
- Using scripts that listen to javascript events triggered.
- Using scripts that modify settings.
- Reading javascript objects.

## URL Query Parameters

### Embed Mode

**Syntax:** `?mode=<mode>`

**Description:** Strips away top navigation, index, table of contents, footer, and others for preview mode.

**See:** [Embed Mode](/support-center/previewing-documentation#embed-mode)

### Disable Scripts

**Syntax:** `?disableScripts=true`

**Description:** Disables scripts temporarily.

**See:** [Disabling HEAD Tags](/support-center/custom-javascript#disabling-head-tags)

### Disable Styles

**Syntax:** `?disableStyles=true`

**Description:** Disables styles temporarily.

**See:** [Disabling Styles](/support-center/custom-css#disabling-styles)

### Personalisation (Clear Text)

**Syntax:** `?vars=<vars>`

**Description:** Personalises the documentation by overriding variables with clear text in JSON format.

**See:** [Personalising through URL](/support-center/personalised-docs#personalising-through-url)

### Personalisation (Base64)

**Syntax:** `?hvars=<vars>`

**Description:** Personalises the documentation by overriding variables with Base64 text.

**See:** [Personalising through URL](/support-center/personalised-docs#personalising-through-url)

### JWT Authentication

**Syntax:** `?jwt=<token>`

**Description:** Securely give access to the docs.

**See:** [auto$](/support-center/custom-login)

### Set Frontend Application Deployment ID

**Syntax:** `?deployment_id=<id>`

**Description:** Sets the frontend application deployment version. Use `latest` for the latest version.

**See:** [Testing CSS](/support-center/custom-css#testing-css)

## JavaScript Functions

### Navigate to URL (Deprecated)

**Function:** `openLink(event, link)`

**Returns:** Nothing.

**Arguments:**

- `event`: The `MouseEvent` or `KeyboardEvent`.
- `link`: Absolute path (without host and basepath) such as `/support-center/developer-tools`.

**See:** [Linking to Content](/support-center/custom-landing-page#linking-to-content)

**Deprecated:** Use [Navigate to Path](/support-center/developer-tools#navigate-to-path) instead.

### Navigate to Path

**Function:** `navigate(link, options ?: {addBasePath: boolean})`

**Returns:** Nothing.

**Arguments:**

- `link`: Absolute path (without host and basepath) such as `/support-center/developer-tools`.
- `options`: (optional)
    - `addBasePath`: Prepends the base path automatically to the link.

**Description:** Navigates to a path internally inside the single page application, without reloading the page.

**See:** [Linking to Content](/support-center/custom-landing-page#linking-to-content)

### Navigate Home

**Function:** `goHome()`

**Returns:** Nothing.

**Arguments:** None.

**Description:** Goes to the landing page, or to the default page if no landing page is set. Equivalent to `openLink('/')` when the project has no basepath.

### Make All Landing Page Links Route in SPA

**Function:** `window.applyClickHandlersOnLinks()`

**Returns:** Nothing.

**Arguments:** None.

**Description:** Captures all absolute paths on a rendered landing page and routes them internally in the single page application rather than a browser tab navigation. Use after all anchor elements have been rendered on a landing page.

**See:** [Custom Landing Page](/support-center/custom-landing-page#adding-javascript)

### Resize Custom HTML iFrame

**Function:** `window.postMessage('resize', '*');`

**Returns:** Nothing.

**Arguments:** Must be provided as is.

**Description:** Informs the parent element to resize because elements have been dynamically added to the iFrame.

**See:** [Resizing Dynamic iFrames](/support-center/custom-html#resizing-dynamic-iframes)

### Apply Advanced Settings

**Function:** `window.settings.apply(settings)`

**Returns:** Nothing.

**Arguments:**

- `settings`: An object containing [specific settings](/support-center/advanced-settings#applying-settings).

**Description:** Modifies UI or functionality, including search, code theme, SEO, and others.

**See:** [Applying Settings](/support-center/advanced-settings#applying-settings)

### Modify UI Text

**Function:** `window.translations.apply(translation)`

**Returns:** Nothing.

**Arguments:**

- `translation`: An object containing [certain UI texts that can be changed](/support-center/ui-translation#which-text-can-be-changed).

**Description:** Modifies UI text, whether for translation or otherwise.

**See:** [auto$](/support-center/ui-translation)

### Register Custom Interceptors

**Function:** `window.registerCustomInterceptor(interceptor)`

**Returns:** Nothing.

**Arguments:**

- `interceptor`: A function with two arguments, `data` and `next`. See [Custom Interceptors](/support-center/try-it-out#how-to-set-up-custom-interceptors).

**Description:** Registers a custom interceptor that can modify API playground requests before they are sent.

### Get Active Project

**Function:** `window.getActiveProject()`

**Returns:** `Project Object {id: number, title: string, slug: string, basepath: string}`

### Get Active Version

**Function:** `window.getActiveVersion()`

**Returns:** `Version Object {id: number, name: string, slug: string, isLatest: boolean, docs: {id: number, title: string, slug: string}[], refs: {id: number, title: string, slug: string}[]}` or `null`

### Get Active Section

**Function:** `window.getActiveSection()`

**Returns:** `Section Object {id: number, title: string, slug: string, type: string, index: any}` or `null`

### Get Active Page

**Function:** `window.getActivePage()`

**Returns:** `Page Object {id: number, title: string, slug: string}` or `null`

### Zoom Image

**Function:** `window.zoomImage(src)`

**Returns:** Nothing.

**Arguments:**

- `src`: The URL of the image to load.

**Description:** Loads the image in an overlay over the docs, just like when native images are clicked in product.

### Zoom Image from within an iFrame

**Function:** `window.postMessage({zoomImage: src}, '*')`

**Returns:** Nothing.

**Arguments:**

- `src`: The URL of the image to load.

**Description:** Loads the image in an overlay over the docs, just like when native images are clicked in product. Use it when the image is created by a [auto$](/support-center/custom-html) which uses an iFrame (when there is a script or iFrame).

### Change Theme

**Function:** `window.setTheme(theme: 'light' | 'dark')`

**Returns:** Nothing.

**Arguments:**

- `theme`: Either `light` or `dark`.

**Description:** Changes the theme for the session.

## JavaScript Dispatched Events

### Landing Page Cards Generated

**Event:** `oncardschanged`

**When:** Landing page is loading.

**Emits:** Details about every documentation and API reference in the default version which make up the cards in the landing page.

**See:** [Adding JavaScript](/support-center/custom-landing-page#adding-javascript)

### Project Loaded

**Event:** `onprojectloaded`

**When:** Project has loaded. DOM elements should already be available now for manipulation if needed.

**Emits:** Nothing.

**See:** [Project Loaded](/support-center/custom-javascript#project-loaded)

### Version Changed

**Event:** `onversionchange`

**When:** Version has changed.

**Emits:** Details about the version that is being switched to.

### Section Changed

**Event:** `onsectionchange`

**When:** Section (documentation or API reference) is changing.

**Emits:** Details about the section that is being switched to.

**See:** [Section Changes](/support-center/custom-javascript#section-changes)

### Page Changed

**Event:** `onpagechange`

**When:** Page is changing.

**Emits:** Details about the page that is being switched to.

**See:** [Page Changes](/support-center/custom-javascript#page-changes)

### Page Loaded

**Event:** `onpageloaded`

**When:** Page has loaded.

**Emits:** Details about the page that has loaded. Note that async-retrieved objects may not have loaded yet, such as images or videos.

### Reference Content Loaded

**Event:** `onreferencecontentloaded`

**When:** Reference has loaded and UI is ready. Also when a tag expands and shows new content.

**Emits:** The HTML element that loaded if you wish to make customisations to the API reference UI, as follows:

{% code %}
{% tab language="json" %}
{
  el: HTMLElement
}
{% /tab %}
{% /code %}

### Search Performed

**Event:** `onsearch`

**When:** Search has been performed.

**Emits:** Details about the query and hits count as follows:

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

### Feedback Submitted

**Event:** `onfeedback`

**When:** Feedback (like/dislike) vote has been registered.

**Emits:** Details about the feedback as follows:

{% code %}
{% tab language="json" %}
{
  action: 'vote',
  vote: boolean, // true for like, false for dislike
  pageUrl: string
}
{% /tab %}
{% /code %}

## JavaScript Objects

### Access Variables

**Object:** `window.vars`

**Description:** Access current variables set in the documentation. Available after the project loads.

**See:** [Using Project Variables in Scripts](/support-center/variables#using-project-variables-in-scripts)