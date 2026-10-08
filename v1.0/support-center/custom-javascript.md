---
type: page
title: Custom HEAD Tags
listed: true
description: 
index_title: Custom HEAD Tags
hidden: false
keywords: 
tags: customisation
---

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Pro Projects
</div>
{% /html %}

Apply project-wide javascript, styles, links, and meta that gets added to the HEAD tag of the page.

## Customising HEAD Tags

To customise HEAD tags:

- Open Project Settings → **Customisation**.
- In the Custom code card, click **Edit HEAD tags**.
- Enter the custom tags as you would in HTML, then click **Save draft** in the top menu. This will save the HTML in draft mode, so you can test it out.
- To publish it to readers, click **Save \& publish**.
- To discard the draft changes, click **Revert**.

All custom tags will only run in live mode, and will not load in editor mode.

## Organisation HEAD Tags

If your projects belong to an organisation, the owner can maintain one set of HEAD tags shared across them from [Organisation Settings](organisation-settings.md#custom-head-tags) → **Custom HEAD tags**.

A project does not inherit them automatically. To opt in, open Project Settings → **Customisation** and turn on **Use organisation HEAD tags**. The organisation's tags are injected before the project's own, so where both set the same thing, the project's wins.

## Using an AI Coding Agent

An AI coding agent such as Claude Code, Cursor or Codex can write the JavaScript for you. Copy the prompt below into your agent and fill in the three lines at the top.

The prompt has the agent read the pages that matter before it writes anything: [Customising Visuals](customising-visuals.md) to check whether a setting already does the job, this page, [Custom CSS](customising-visuals/custom-css.md), [Developer Tools](developer-tools.md) and [Popular Customisations](css-customisations.md). For anything else, it starts from this site's [llms.txt](ai-features/llms-txt.md).

{% code %}
```none {% title="Prompt" %}
I want to customise my DeveloperHub docs with Custom CSS or Custom HEAD tags (JavaScript).

What I want: <describe the change>
My docs URL: <https://docs.example.com>
My UI: <Matcha, Next or Original>

Before writing any code, read these pages:
- https://docs.developerhub.io/support-center/customising-visuals.md (built-in settings that need no code)
- https://docs.developerhub.io/support-center/custom-css.md (Custom CSS rules and CSS variables)
- https://docs.developerhub.io/support-center/custom-javascript.md (Custom HEAD tags rules and events)
- https://docs.developerhub.io/support-center/developer-tools.md (functions, events and objects available to scripts)
- https://docs.developerhub.io/support-center/css-customisations.md (worked examples)
To look up anything else, start from https://docs.developerhub.io/llms.txt.

Then:
1. If a built-in setting already does what I want, tell me which one and stop.
2. Use Custom CSS wherever CSS can do it. Use Custom HEAD tags only for what needs JavaScript.
3. Find the real selectors on my docs. If you can open a browser, inspect the page yourself. If not, ask me to paste the element's HTML from my browser's developer tools.
4. Nothing is compiled, so use only CSS and JavaScript that Chrome and Edge 98, Firefox 104 and Safari 15.4 support. That means no CSS nesting, :has() or container queries.
5. Scope every CSS rule under .customise.live with a specific selector. Never restyle generic selectors such as p, table, img or .container. Prefer the documented CSS variables, and set dark theme values under .dark-mode.
6. Put scripts inside <script> tags, without async or defer. Inline scripts cannot use import, export or top-level await, and their top-level let and const stay inside their own tag, so share values through window. The site is a single page application, so hook into the documented events (onprojectloaded, onpagechange) instead of DOMContentLoaded or load.
7. Make it work on phone, tablet and desktop, and in both light and dark theme.
8. Give me the final code ready to paste, say which box it goes in (Custom CSS or Custom HEAD tags), and explain how to test it before I publish.
```
{% /code %}

{% callout title="No web access?" %}
If your agent cannot open web pages, open each link in the prompt yourself and paste the contents in after the prompt.
{% /callout %}

Paste the tags it returns into Custom HEAD tags, then [test them](custom-javascript.md#testing-head-tags) with **Save draft** before you publish. If something breaks, [disable the HEAD tags](custom-javascript.md#disabling-head-tags) in your browser to check whether they are the cause.

## Tags Format

Tags should be added fully as they would exist in HEAD, such as:

{% code %}
```markup {% title="HTML" %}
<!-- Script to install jquery -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

<!-- Install Bootstrap CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">

<!-- Add your own CSS - You can also do that through Custom CSS -->
<style>
  .my-container{
    width: 100%;
  }
</style>

<!-- Add meta such as OpenGraph title -->
<meta property="og:title" content="X Documentation">
```
{% /code %}

Do not add any `<body>`, `<html>` or other tags that do not naturally exist in HEAD.

{% callout type="warning" title="Warning" %}
Do not use async or defer in your scripts. Scripts will be loaded async regardless.
{% /callout %}

{% callout type="warning" title="Supported JavaScript" %}
Scripts run exactly as you write them; we do not compile them. Use only JavaScript that our [supported browsers](supported-browsers.md) run.
{% /callout %}

{% callout title="Each script runs on its own" %}
Inline scripts cannot use `import`, `export` or top-level `await`. To load a library, add it with `<script src="...">`. Top-level `let`, `const` and `class` declarations stay inside their own `<script>` tag, so to share something between tags, attach it to `window`.
{% /callout %}

## Why add scripts?

By adding scripts, you can do more with your documentation:

- Install third party services for tracking, analysing, interacting with your readers.
- Create scripts that interact with [Custom HTML](custom-html.md) in the pages or [Custom Landing Page](landing-page/custom-landing-page.md).
- Add javascript redirection rules.
- Add your own icon set using CSS.
- Enhance your [SEO](seo.md) by adding the relevant META tags to your business.
- Change the [UI Text](customising-visuals/ui-translation.md).

## External Hooks

There are several events that are triggered by %product% which can help you achieve the level of customisation you need. The full list of hooks is available at [Javascript Dispatched Events](developer-tools.md#javascript-dispatched-events).

### Project Loaded

To listen to when a project loads, which is also when most elements of the page also are loaded, you may listen to a custom event on document called `onprojectloaded`. An example:

{% code %}
```markup
<script>
	document.addEventListener('onprojectloaded', function () {
    const topnav = document.querySelector(".topnav"); // .topnav is loaded at this time, probably not before this.
    topnav.classList.add('wide');
  });
</script>
```
{% /code %}

If you are aiming at modifying the top navigation, then you should use this event.

{% callout type="warning" title="Use `onprojectloaded` instead of `document.onload`." %}
Because %product% is a single page application, `document.onload` has no effect in Custom HEAD tags. All Custom HEAD tags are actually loaded after `document.onload` is called. Use `onprojectloaded` whenever you need to use `document.onload`.
{% /callout %}

### Section Changes

To listen to when a section (landing page, documentation) changes, you may listen to a custom event on document called `onsectionchange`. An example:

{% code %}
```markup
<script>
	document.addEventListener('onsectionchange', function (event) {
        switch (event.detail.type) {
            case 'landing-page':
                // It is a landing page
                break;
            case 'documentation':
                // It is a documentation
                break;
            case 'reference':
                // It is a reference
                break;
            }
    });
</script>
```
{% /code %}

If the section changed is a documentation, then the indices are also listed.

### Page Changes

To listen to when a page changes, you may listen to a custom event on document called `onpagechange`. An example:

{% code %}
```markup
<script>
	document.addEventListener('onpagechange', function (event) {
        console.log(event.detail.slug); // e.g. getting-started
    });
</script>
```
{% /code %}

### Redirection Rules

Using Custom JS, you can setup front-end redirection rules. For example, if you want to redirect one of your projects which has semantic versioning less than 1.0 to another, you might want to use something like this:

{% code %}
```markup
<script>
	const redirectDocs = function() {
		const regex = /^\/([0-9\.]+)\//i;
		const path = window.location.pathname;
		if ((match = regex.exec(path))) {
			const redirectPath = match[0];
			const version = match[1];
			const semver = version.split('.');
			if (semver[0] < 1) {
				window.location.href = "https://alpha.always-blue.io"+redirectPath;
			}
		}
	}

	redirectDocs();	
</script>
```
{% /code %}

Or if you have changed a documentation slug, then you might want to redirect to the new slug:

{% code %}
```markup
<script>
	const redirectDocs = function() {
		const oldDoc = "/old-doc-slug";
		const newDoc = "/new-doc-slug";
		const path = window.location.pathname;
		if (path.includes(oldDoc)) {
			window.location.pathname = path.replace(oldDoc, newDoc);	
		}
	}
	redirectDocs();	
</script>
```
{% /code %}

If you need more powerful redirection rules, then check [server-side 301 redirect rules](hosting/url-redirects.md).

### Custom Landing Page Loaded

See [Custom Landing Page](landing-page/custom-landing-page.md).

## Testing HEAD Tags

HEAD tags do not run in the editor, so test a draft on your published docs:

1. Edit the HEAD tags, then click **Save draft** in the top menu. Readers keep getting the published tags.
2. Click **See draft project** in the notice above the tags. Your docs open with the draft tags running, framed in blue, with a dock at the bottom listing the drafts you are viewing.
3. When everything works, click **Save \& publish**.

Docs you open from the editor keep running your drafts this way. To see a page as readers do, click **View as Reader** in the dock, or open the docs in an incognito window.

## Disabling HEAD Tags

For testing if a script or style in HEAD tags is causing issues, you might want to disable all HEAD tags momentarily only for your browser. To do this, append a query `?disableScripts=true` to any published docs URL.

For example, if your docs are available on `https://example.com/docs` then you can disable HEAD tags for your session using `https://example.com/docs?disableScripts=true`.

Once you refresh the page without `disableScripts=true`, HEAD tags will be enabled again.
