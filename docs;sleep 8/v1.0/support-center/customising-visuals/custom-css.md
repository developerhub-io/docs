---
type: page
title: Custom CSS
listed: true
slug: custom-css
description: Apply project-wide CSS changes and have complete design control using Custom CSS. Learn how to customize CSS, test it, revert changes, and more.
index_title: Custom CSS
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

Apply project-wide CSS changes and enable complete design control using Custom CSS.

{% callout type="info" title="Need to be more specific?" %}
If you wish to apply (or test) on a version, then you can use the selector `.customise .version-{{versionSlug}}`.
{% /callout %}

## Customising CSS

To customise CSS:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the Sidebar.
- Under Customise, select Edit CSS.
- Enter the custom CSS, and click Save. This will save the CSS in draft mode, so you can test it out.
- To publish it to readers, click Save & Publish.
- To revert the draft changes, click Revert.

The CSS will be applied immediately.

## Testing CSS

You probably want to test your CSS changes before shipping them to your customers. To test CSS, click on Save in the Custom CSS window. At this stage, the CSS will be applied immediately inside the editor. Also, if you use any of the Go To buttons from the sidebar, then you will also see the CSS changes on the published docs.

If you want to double check what your readers see after you click the Go To button, then open the published docs in an incognito window of your browser.

You can revert the changes from the Custom CSS window.

{% callout type="warning" title="Reverting Draft CSS" %}
When you revert the CSS, the draft changes are discarded and lost.
{% /callout %}

{% callout type="info" title="Testing while frontend application is pinned" %}
To test latest frontend application on the readers site if your [frontend application is pinned](/support-center/custom-css#pinning-frontend-application-version), add `?deployment_id=latest` to the URL. To confirm which application version is being used, check the `X-DeveloperHub-Version` header in the first network request.
{% /callout %}

## Testing Dark Theme

To test dark theme without enabling it for your readers, use [Change Theme](/support-center/developer-tools#change-theme) function to apply the theme without modifying the project settings.

## Disabling Styles

For testing if a style applied using Custom CSS is causing issues, you might want to disable all custom styles momentarily only for your browser. To do this, append a query `?disableStyles=true` to any published docs URL.

For example, if your docs are available on `https://example.com/docs` then you can disable customs styles for your session using `https://example.com/docs?disableStyles=true`.

Once you refresh the page without `disableStyles=true`, custom styles will be enabled again.

## Why customise CSS?

By customising CSS, you can:

- Apply an image to the navigation header.
- Change the index style.
- Add icons to categories in the index, or apply a smooth colour transform like in our docs.
- Animate buttons.
- Import another CSS file using `@import url(...)` .
- Use your own [custom (non Google Font) font](https://developerhub.io/blog/using-your-own-font/).
- Create a custom landing page, removing sidebars and titles.
- Change the [code theme](/support-center/code-theme).
- Or anything you can think of, really...

{% callout type="warning" title="Warning" %}
The CSS is not encapsulated and applies globally. %product% CSS does change frequently, and we cannot guarantee consistent design (check [Pinning Frontend Application Version](/support-center/custom-css#pinning-frontend-application-version)). You might want to add `!important` to your styles.
{% /callout %}

## CSS Best Practices

%product% CSS is not encapsulated and applies globally. This means that you can change everything - including what you see in the editor, including the editor itself! With this amount of great power, comes great responsibility, so make sure you follow these best practices. The examples will work through one case: "How to change the colour of the page title".

{% callout type="warning" title="Ensure Cross-Platform Compatibility" %}
Ensure that any Custom CSS changes adhere to all display sizes and input devices. The default CSS is designed to work for phones, tablets, laptop screens and large screens. **Always test the CSS changes you make on all sizes to ensure reader satisfaction.**
{% /callout %}

### {% badge type="custom" text="1" /%} Use `.customise`

`.customise`  is a CSS selector which you should probably use on all your CSS rules. `.customise` encapsulates everything that the editor is not, which is everything you might want to customise. For example:

{% code %}
{% tab language="css" %}
/* DON'T DO THIS ❌ - Will change all heading 1 everywhere, in editor, in dashboard... horrible */
h1 {
  color: green !important;
}

/* PREFER TO DO THIS - Will change all heading 1 only where it is expected to be changed */
.customise h1 {
  color: green !important;
}
{% /tab %}
{% /code %}

### {% badge type="custom" text="2" /%} Use `.live`

`.live`  is a CSS selector which you should probably use on all your CSS rules. `.live` encapsulates CSS that only loads on your live docs site, but not when in the editor. Changing the page styles in the editor could cause inconsistencies and features to break if CSS is not very carefully written, so it is best to only have these styles apply on the live docs site. For example:

{% code %}
{% tab language="css" %}
/* DON'T DO THIS ❌ - Will change all heading 1 only in live docs site and editor */
.customise h1 {
  color: green !important;
}

/* PREFER TO DO THIS - Will change all heading 1 only in the live docs site */
.customise.live h1 {
  color: green !important;
}
{% /tab %}
{% /code %}

### {% badge type="custom" text="3" /%} Use specific selectors

In our previous examples, `h1` is quite a vague selector. If we want to change the page title colour, then it's best to use it's specific selector and only in Documentation.

{% code %}
{% tab language="css" %}
/* DON'T DO THIS ❌ - Will change all heading 1 only in live docs site */
.customise.live h1 {
  color: green !important;
}

/* DO THIS INSTEAD ✅ - Will change the page title only in Documentation in the live docs site */
.customise.live .documentation .title-container>.title {
  color: green !important;
}
{% /tab %}
{% /code %}

{% callout type="error" title="Do Not Change Generic Styles" %}
Changing the CSS of generic selectors like `table`, `p`, `.container`, `.row`, `img`, etc... will modify the global look and would probably break functionality of both the editor and the live view. We use Bootstrap heavily and changing its standard styles is not recommended. Instead, find a specific selector to apply the styles on.

If you are creating a landing page, then create specific selectors. For example, if you wanted to use a `.container`, then also add a `.x-container` selector on the container, and apply the styles on `.x-container` instead of the generic `.container`.
{% /callout %}

## CSS Customisation Examples

See [auto$](/support-center/css-customisations).

## Examples on Page

As we do not want to change the style of our documentation (since we love it so much), we'll show some styled items here.

- Sign up now button with hover effect.

{% html %}
<div class="text-left">
<a class="doc-button" href="https://app.developerhub.io/signup" target="_blank">Sign up now 🚀</a>
</div>
{% /html %}

- Links to other documentations.

{% html %}
<div class="row">

	<div class="col text-left px-2 py-3 mx-3 doc-lg-button">

		<a href="https://docs.developerhub.io" _target="blank">

			<i class="fas fa-book fa-2x ml-2 mr-2"></i>

			<div class="d-inline" style="font-size: 1.3em; color: var(--font-color)">Documentation</div>

		</a>

	</div>

	<div class="col text-left px-2 py-3 mx-3 doc-lg-button">

		<a href="https://swagger.developerhub.io" _target="blank">

			<i class="fas fa-vector-square fa-2x ml-2 mr-2"></i>

			<div class="d-inline" style="font-size: 1.3em; color: var(--font-color)">Reference</div>

		</a>

	</div>

</div>
{% /html %}

- Sign up forms.

{% html %}
<div class="container pt-3 pb-5" style="background: hsl(33, 100%, 98%); border-radius: 12px">

	<div class="row">

		<div class="col text-center">

			<div class="mt-2" style="font-size: 1.5em; color: #333">Sign up for our updates</div>

			<p style="color: #333">We'll send you updates every week</p>

		</div>

	</div>

	<div class="row">

		<div class="col text-center">

			<input type="text" class="d-inline-block doc-input"/><button class="doc-button" onclick="alert('Gotcha');">Sign up</button>

		</div>

	</div>

</div>
{% /html %}

## CSS Variables

We have set up variables for you to change, so you can change the look and feel easily. When [theme](/support-center/theme) is set, those variables automatically get modified.

{% code %}
{% tab language="css" %}
:root {
  --brand: #5368e7; /* Your brand color - auto assigned from project */
  --brand-transparent: #5368e754; /* Your brand color with transparency - auto assigned from project */
  --reference-hue: 230; /* Your brand color's hue - used in reference right column */
  --font: Nunito, "SansSerif"; /* Your font - auto assigned from project */
  --font-size: 15px; /* Font size for page content */
  --secondary-font-size: 16px; /* Font size for index content */
  --link: #ff536b; /* Your link color - auto assigned from project */
  --inline-code: #444444; /* Your inline code color */
  --inline-code-bg: #f5f7f7; /* Your inline code background color */
  --nav-link: #FFFFFF; /* Your navigation link color - auto generated from brand and link colour */
  --dominant: #5368e7; /* Your dominant colour - auto generated from brand and link colour */
  --code-font: Roboto Mono,Consolas,Monaco,Andale Mono,Ubuntu Mono,monospace; /* Font used for code blocks */
  --code-font-size: 13px; /* Size of font used for code blocks */
  
  --bg-color: #FFF; /* Background color */
  --alt-bg-color: #FFF;  /* Used in some controls for differentiating from background color in dark mode */
  --font-color: #333; /* Font color */
  --heading-color: #444; /* Heading color */
  --category-color: #555; /* Category (in index) color */
  --toc-link-color: #666;  /* TOC text color */
  --table-second-color: #FAFAFA;  /* Alternating table background color */
  --page-border-color: #F1F1F1;  /* Left and bottom page border color */
  
  --index-width: calc(var(--secondary-font-size) * 18); /* Width of documentation index */
  --reference-index-width: calc(var(--secondary-font-size) * 16); /* Width of reference index */
  
  --dropdown-animation: dropdownIn 500ms cubic-bezier(0, 1, 0.4, 1); /* Animation when dropdown opens */
}

.customise .references {
  --required-text: '*'; /* Text that shows to denote that a field is required in request/response bodies */
}
{% /tab %}
{% /code %}

To modify the variables used when dark theme is enabled, use the selector `.dark-mode`, for example:

{% code %}
{% tab language="css" %}
.dark-mode {
  --brand: #123456;
  --link: blue;
}
{% /tab %}
{% /code %}

### Font Weights

If your assigned font does not have all the weights we use on %product% then you can reassign some weights to another:

{% code %}
{% tab language="css" %}
:root {
  --fw-100: 100;
  --fw-200: 200;
  --fw-300: 300;
  --fw-400: 400;
  --fw-500: 500;
  --fw-600: 600;
  --fw-700: 700;
  --fw-800: 800;
  --fw-900: 900;
}
{% /tab %}
{% /code %}

For example, if weight 500 does not exist, then you may set `--fw-500: 600`, so font weight 600 is used whenever 500 is expected.

{% callout type="warning" title="Other variables" %}
We have more variables which are not mentioned here, such as `--shadeX` and `--helperX` which are not built to be modified by the user. Changing them will definitely lead to unexpected results.
{% /callout %}

## Pinning Frontend Application Version

As we build out new features for %product%, we might change the DOM, CSS and javascript we ship that makes up your docs site. These changes might interfere with your custom CSS changes (if you have heavy changes) and cause unexpected site style.

To prevent this from happening, you can pin the frontend application version to a certain deployment. That means that any change we make to the single-page application would not be reflected to your readers. We also might pin your frontend application version automatically when we do big changes that may affect any custom CSS changes.

To pin your frontend application version:

- From the left sidebar, click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Advanced Settings, click the button next to Pin frontend application version.
- Choose a version according to its date and description.

To unpin the frontend application version, choose Latest version.

Change might take up to 5 minutes to reflect on the docs site. The change only reflects on the readers site, not in the editor.

{% callout type="warning" title="Important" %}
While this ensures that your reader does not see unexpected styles, this also stops all updates to your docs site. **You are expected to modify the custom CSS as soon as possible and return to Latest version.** We do not guarantee that older versions will remain functioning.
{% /callout %}

## Migrating to Latest Frontend Application Version

If you are pinned to a different application version and wish to move to the latest frontend application version in order to get the latest features, do the following:

1. **Test how the docs would look with latest frontend application version**

To test latest frontend application on the readers site if your frontend application is pinned, add `?deployment_id=latest` to the URL. To confirm which application version is being used, check the `X-DeveloperHub-Version header` in the first network request.

Load at least the landing page, documentation page and API reference with `?deployment_id=latest` at the end of the URL and check if the pages look as expected. Otherwise, modify the CSS/JS in [draft mode](/support-center/custom-css#testing-css) and keep on iterating until the pages look perfect.

{% callout type="info" title="?deployment_id=latest is temporary" %}
Make sure that everytime you reload the page and wish to see it in latest application version, you add `?deployment_id=latest`.
{% /callout %}

2. **Publish CSS/JS changes**

As your CSS/JS changes are now perfect, publish them to your readers.

3. **Unpin frontend application version**

To unpin your frontend application version:

- From the left sidebar, click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Advanced Settings, click the button next to Pin frontend application version.
- Choose "Latest".