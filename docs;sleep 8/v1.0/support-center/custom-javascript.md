---
type: page
title: Custom HEAD Tags
listed: true
slug: custom-javascript
description: 
index_title: Custom HEAD Tags
hidden: 
keywords: 
tags: customisation
---

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

Apply project-wide javascript, styles, links, and meta that gets added to the HEAD tag of the page.

## Customising HEAD Tags

To customise HEAD tags:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the Sidebar.
- Under External Integrations, select **Custom HEAD Tags** {% icon classes="fab fa-js-square" /%}
- Enter the custom tags as you would in HTML, and click Save. This will save the HTML in draft mode, so you can test it out.
- To publish it to readers, click Save & Publish.
- To revert the draft changes, click Revert.

All custom tags will only run in live mode, and will not load in editor mode.

## Tags Format

Tags should be added fully as they would exist in HEAD, such as:

{% code %}
{% tab language="markup" title="HTML" %}
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
{% /tab %}
{% /code %}

Do not add any `<body>`, `<html>` or other tags that do not naturally exist in HEAD. 

{% callout type="warning" title="Warning" %}
Do not use async or defer in your scripts. Scripts will be loaded async regardless.
{% /callout %}

{% callout type="error" title="Only ES5" %}
To ensure compatibility with all browsers, do not add any scripts that contain any syntax that is not supported by ECMAScript 5 (ES5, ECMAScript 2009). We do not automatically check or compile into ES5. Failure to do so may render your site unusable to some or all users.
{% /callout %}

## Why add scripts?

By adding scripts, you can do more with your documentation:

- Install third party services for tracking, analysing, interacting with your readers.
- Create scripts that interact with [auto$](/support-center/custom-html) in the pages or [Custom Landing Page](/support-center/custom-landing-page).
- Add javascript redirection rules.
- Add your own icon set using CSS.
- Enhance your [SEO](/support-center/seo) by adding the relevant META tags to your business.
- Change the [UI Text](/support-center/ui-translation).

## External Hooks

There are several events that are triggered by %product% which can help you achieve the level of customisation you need. The full list of hooks is available at [Javascript Dispatched Events](/support-center/developer-tools#javascript-dispatched-events).

### Project Loaded

To listen to when a project loads, which is also when most elements of the page also are loaded, you may listen to a custom event on document called `onprojectloaded`. An example:

{% code %}
{% tab language="markup" %}
<script>
	document.addEventListener('onprojectloaded', function () {
    const topnav = document.querySelector(".topnav"); // .topnav is loaded at this time, probably not before this.
    topnav.classList.add('wide');
  });
</script>
{% /tab %}
{% /code %}

If you are aiming at modifying the top navigation, then you should use this event.

{% callout type="warning" title="Use `onprojectloaded` instead of `document.onload`." %}
Because %product% is a single page application, `document.onload` has no effect in Custom HEAD tags. All Custom HEAD tags are actually loaded after `document.onload` is called. Use `onprojectloaded` whenever you need to use `document.onload`.
{% /callout %}

### Section Changes

To listen to when a section (landing page, documentation) changes, you may listen to a custom event on document called `onsectionchange`. An example:

{% code %}
{% tab language="markup" %}
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
{% /tab %}
{% /code %}

If the section changed is a documentation, then the indices are also listed.

### Page Changes

To listen to when a page changes, you may listen to a custom event on document called `onpagechange`. An example:

{% code %}
{% tab language="markup" %}
<script>
	document.addEventListener('onpagechange', function (event) {
        console.log(event.detail.slug); // e.g. getting-started
    });
</script>
{% /tab %}
{% /code %}

### Redirection Rules

Using Custom JS, you can setup front-end redirection rules. For example, if you want to redirect one of your projects which has semantic versioning less than 1.0 to another, you might want to use something like this:

{% code %}
{% tab language="markup" %}
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
{% /tab %}
{% /code %}

Or if you have changed a documentation slug, then you might want to redirect to the new slug:

{% code %}
{% tab language="markup" %}
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
{% /tab %}
{% /code %}

If you need more powerful redirection rules, then check [server-side 301 redirect rules](/support-center/url-redirects).

### Custom Landing Page Loaded

See [Custom Landing Page](/support-center/custom-landing-page).

## Staging Environment

There is no staging environment for testing HEAD tags changes at this moment. However, you can set up a new project and test the HEAD tags on it before applying it on your production project. [Let us know ](/support-center/contact-us) if you needed help in setting up the project.

## Disabling HEAD Tags

For testing if a script or style in HEAD tags is causing issues, you might want to disable all HEAD tags momentarily only for your browser. To do this, append a query `?disableScripts=true` to any published docs URL.

For example, if your docs are available on `https://example.com/docs` then you can disable HEAD tags for your session using `https://example.com/docs?disableScripts=true`.

Once you refresh the page without `disableScripts=true`, HEAD tags will be enabled again.