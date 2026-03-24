---
type: page
title: Custom Landing Page
listed: true
slug: custom-landing-page
description: 
index_title: Custom Landing Page
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

If you wish to have more control and branding over your landing page, you may use HTML, CSS and Javascript to craft a custom landing page.

{% image url="https://image-archive.developerhub.io/image/upload/27830/giywcgidtrajyrzmqrih/1586529385.jpg" caption="Our Custom Landing Page" mode="responsive" height="1189" width="1501" %}
{% /image %}

## Use Custom Landing Page

To enable a custom landing page for the main landing page:

- Open Landing Page from the sidebar {% icon classes="fas fa-rocket inv-icon" /%}
- Choose the main landing page.
- Click on the {% icon classes="fas fa-cog" /%} settings icon at the top.
- Click on **Enable** next to Use Custom Page.

To modify the landing page HTML:

- Click **Edit HTML**.

{% image url="https://uploads.developerhub.io/prod/02/9qnjmb6yys60jmptwoto2ymwoa0hp23qinnli89kmege90vrp9gkbsgu4sy51zcz.png" mode="responsive" height="794" width="1198" %}
{% /image %}

- Paste or type in the HTML that will make your custom landing page. Click Save. This will save the HTML in draft mode, so you can test it out.
- To publish it to readers, click Save & Publish.
- To revert the draft changes, click Revert.

{% callout type="warning" title="Write body only - Not full HTML page" %}
The HTML you provide will be inserted into the body of the landing page in a div with `landing-page-container` class. Thus, do not wrap everything in `<html>` tag. `<head>` tag will also be discarded. See our examples [below](/support-center/custom-landing-page#mocking-default-landing-page).

This also apply to `<style>`. All styles should be moved to [Custom CSS](/support-center/custom-css).
{% /callout %}

## Crafting a Landing Page

{% image url="https://image-archive.developerhub.io/image/upload/27830/dpvldj3gudm4i4lokx8j/1586528975.jpg" mode="responsive" height="507" width="914" %}
{% /image %}

When customising the landing page, you may enter HTML that will be inserted asynchronously in your landing page.

{% callout type="warning" title="Unvalidated HTML" %}
Note that we do not evaluate or validate the HTML inserted - please double check that it is valid.
{% /callout %}

## Adding CSS

If you wish to add CSS, then you can add it to [Custom CSS](/support-center/custom-css), or you could add it in [Custom HEAD Tags](/support-center/custom-javascript) in a `<style>` tag, or even link external CSS by using `<link>` tag.

{% callout type="warning" title="Global CSS" %}
Remember that the CSS is applied globally. Modifying classes of conventional names (specially Bootstrap selectors), such as `.container` might have unwanted effects.
{% /callout %}

## Adding Javascript

If you wish to add Javascript, then you can add it in [Custom HEAD Tags](/support-center/custom-javascript) in a `<script>` tag. If you wish to reuse the [cards](/support-center/landing-page) from our original landing page, then you can listen to a dedicated event `oncardschanged` as such:

{% code %}
{% tab language="html" %}
<script>
document.addEventListener('oncardschanged', function (event) {
  console.log("cards changed", event);
});
</script>
{% /tab %}
{% /code %}

This event also indicates that the landing page HTML has already loaded, and that you can query its selectors.

The event output looks like the follows for the main landing page:

{% code %}
{% tab language="json" %}
CustomEvent {
  "detail": {
    "sectionType": "landing-page"
    "docs": [
      {
        "title": "Start Here",
        "link": "/support-center",
        "details": [
           {"title": "Getting Started", "link": "/support-center/getting-started"},
           {"title": "Writing Documentation", "link": "/support-center/writing-documentation"},
           {"title": "Structuring Documentation", "link": "/support-center/structuring-documentation"}
        ]
      },
      {
        "title": "Blocks",
        "link": "/support-center",
        "details": [
           {"title": "Code Blocks", "link": "/support-center/code-blocks"},
           {"title": "Callouts", "link": "/support-center/callouts"},
           {"title": "Images", "link": "/support-center/images"}
        ]
      },
    ],
    "refs": [
      {
        "title": "API", 
        "link": "/api"
      }
    ]
  }
}
{% /tab %}
{% /code %}

For a non-main landing page, the detail would be as such:

{% code %}
{% tab language="json" %}
CustomEvent {
  "detail": {
    "sectionType": "custom-page",
    "sectionId": 612
    "docs": [
      {
        "title": "Start Here",
        "link": "/support-center",
        "details": [
           {"title": "Getting Started", "link": "/support-center/getting-started"},
           {"title": "Writing Documentation", "link": "/support-center/writing-documentation"},
           {"title": "Structuring Documentation", "link": "/support-center/structuring-documentation"}
        ]
      },
      {
        "title": "Blocks",
        "link": "/support-center",
        "details": [
           {"title": "Code Blocks", "link": "/support-center/code-blocks"},
           {"title": "Callouts", "link": "/support-center/callouts"},
           {"title": "Images", "link": "/support-center/images"}
        ]
      },
    ],
    "refs": [
      {
        "title": "API", 
        "link": "/api"
      }
    ]
  }
}
{% /tab %}
{% /code %}

Where `sectionId` is an identifier you may use to customise what elements are added to which landing page.

## Linking to Content

To navigate to content in the documentation from your landing page, use absolute paths. When using absolute paths, the navigation would be done internally in the single-page application, rather than a full-slow navigation. For example:

{% code %}
{% tab language="markup" title="HTML" %}
<a href="/support-center/getting-started">
  Getting Started
</a>
<!-- If your project has a basepath (e.g. docs), include it -->
<a href="/docs/support-center/example-requests">
  Example Requests
</a>

<!-- ❌ do not use for internal navigation -->
<a href="https://docs.example.com/support-center/getting-started">
  Example Requests
</a>
{% /tab %}
{% /code %}

If you are creating the content dynamically using Javascript, you can use `window.applyClickHandlersOnLinks()` at the end of your javascript (when all anchors have been added) to make all absolute path links navigate internally:

{% code %}
{% tab language="javascript" %}
const anchor = document.createElement('A');
anchor.href = "/support-center/getting-started";

window.applyClickHandlersOnLinks();
{% /tab %}
{% /code %}

{% callout type="warning" title="Deprecated" %}
Previously, `openLink` function used to handle opening internal links. This is no longer required and such functions can be removed.
{% /callout %}

## Tips & Tricks

### Hiding Top Navigation Bar

If you wish to hide the top navigation bar when on the custom landing page, you can do that using Javascript:

{% code %}
{% tab language="html" %}
<script>
	document.addEventListener('onsectionchange', function (event) {
        switch (event.detail.type) {
            case 'landing-page':
                document.querySelector("app-top-nav").style.display = "none";
                break;
            default:
                document.querySelector("app-top-nav").style.display = "inline";
            }
    });
</script>
{% /tab %}
{% /code %}

## Mocking default Landing Page

See [auto$](/support-center/mocking-default-landing-page) for step-by-step instructions on how to create a landing page like our own.