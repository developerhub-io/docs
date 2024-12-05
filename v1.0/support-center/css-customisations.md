---
type: page
title: Popular Customisations
listed: true
slug: css-customisations
description: Learn how to customize your docs using Custom CSS. Hide version selector, section selector, make top navigation sticky, decrease font size, move index, set theme and more.
index_title: Popular Customisations
hidden: 
keywords: 
tags: customisation
---

You can customise your docs using [auto$](/support-center/custom-css) and [Custom Javascript](/support-center/custom-javascript). Below are some of the most used customisations:

## Hide version selector/picker

{% code %}
{% tab language="css" %}
.customise.live .version-picker {
    display: none;
}
{% /tab %}
{% /code %}

## Hide section/documentation selector/picker

{% code %}
{% tab language="css" %}
.customise.live .section-picker-container {
    display: none;
}
{% /tab %}
{% /code %}

## Make top navigation sticky

{% callout type="warning" title="Only in Original UI" %}
Only apply this customisation for the original UI. For Next UI, there's a setting under Project Settings &gt; Customisations to enable it.
{% /callout %}

{% code %}
{% tab language="css" %}
@media (min-width: 1024px) {
  .customise.live .topnav-container {
    position: fixed;
    top: 0;
    height: auto;
    z-index: 10;
  }

  .customise.live .mega-container {
    margin-top: 70px;
  }

  .customise.live .stick-top {
    top: 70px !important;
  }
}
{% /tab %}
{% /code %}

When navigation is sticky, the scrolling behaviour must be modified in order for headings not to hide under the navigation when it is scrolled to. Add the following to Custom HEAD tags to modify scrolling offsets:

{% code %}
{% tab language="html" %}
<script>
  window.settings.apply({
    scrolling: { // Modify values as needed, according to your navbar height.
      scrollTopOffsetOnFragmentChange: {documentation: -90, apiReference: -50}
    }
  });
</script>
{% /tab %}
{% /code %}

## Decrease top navigation links font-size

Use if the titles are too long and they're breaking into two lines.

{% code %}
{% tab language="css" %}
.customise.live .topnav-container .links {
  font-size: 13px; /* Original is 14px */
}

.customise.live .topnav-container .links .link {
  font-size: inherit;
}
{% /tab %}
{% /code %}

## Move index and table of contents to edges of screen

{% callout type="warning" title="Deprecated" %}
This is enabled by default now.
{% /callout %}

{% code %}
{% tab language="css" %}
.customise.live .container.doc-container {
  max-width: 100%;
}

.customise.live .container.doc-container > .row {
  justify-content: space-between;
}


.customise.live .documentation {
  padding-left: 0;
}
{% /tab %}
{% /code %}

## Set theme automatically according to user preferences

Place in Custom HEAD tags. Only use one of the if conditions.

{% code %}
{% tab language="html" %}
<script>
  // If your theme is set to dark by default, use the following IF condition.
  if (window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches) {
    window.setTheme('light');
	}
  
  // If your theme is set to light by default, use the following IF condition.
  if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
    window.setTheme('dark');
	}
</script>
{% /tab %}
{% /code %}

## Append contact us to search box on no results

Place in Custom HEAD tags.

{% code %}
{% tab language="html" %}
<style>
  .search-contact-us {
    color: inherit;
    font-size: inherit;
    text-decoration: underline;
  }
  
  .search-contact-us:hover {
    color: inherit;
  }
</style>

<script>
  document.addEventListener('onsearch', function (event) {
    let searchEl = document.querySelector('.topnav .search');

    setTimeout(() => {
      if (!document.querySelector('.search-results-container .result')) {
          document.querySelector('.search-results-container .count').innerHTML = 
            'No search results found. <a class="search-contact-us" href="/support-center/contact-us">Contact us?</a>';
      }
    });
  });
</script>
{% /tab %}
{% /code %}

## Hide version warning banner for a specific version

Place in Custom HEAD tags.

{% code %}
{% tab language="html" %}
<script>
document.addEventListener('onsectionchange', e => {
  let versionWarningEl = document.querySelector('.version-warning');
  if (!versionWarningEl) {
    return;
  }

  if (window.getActiveVersion().slug === 'v4') {
    console.log('Hiding banner');
    versionWarningEl.classList.add('d-none');
  } else {
    versionWarningEl.classList.remove('d-none');
  }
});
</script>
{% /tab %}
{% /code %}

## Collapse Section Picker into Dropdown on Next UI

Place in Custom CSS.

{% code %}
{% tab language="css" %}
.customise.live .section-links-group {
  display: none !important;
}

.customise.live app-section-picker.d-mobile {
    display: inline-block !important;
}

@media (min-width: 768px) {
  .customise.live .version-selector-group {
    padding: 8px 0;
  }
}
{% /tab %}
{% /code %}

## Blur Top Navigation Bar

Place is Custom CSS. You might need to handle light theme separately.

{% code %}
{% tab language="css" %}
.customise.live .topnav-container {
    background-color: transparent;
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    -moz-backdrop-filter: blur(10px);
    border-bottom: 1px solid #44444433;
}

.customise.live .external-search.dark {
    background: #00000033;
}
{% /tab %}
{% /code %}

## Adding Icons to Index

To add an icon in place of the expander icon for categories and parent pages in the index, add such CSS:

{% image url="https://uploads.developerhub.io/prod/02/df56hu6n1hk8hmm0l8asvx15zh6t8sbldfrl0x9ta42vo91c02k2vy5e8xh4478v.png" mode="responsive" height="70" width="129" %}
{% /image %}

{% code %}
{% tab language="css" %}
/* First hide the expander icons. You could do this individually or for all expanders */
.customise .sidebar .node_XXXXX>.node-wrapper>.node-content-wrapper>.expander-icon>i {
		display: none;
}

/* To add an emoji */
.customise .sidebar .node_XXXXX>.node-wrapper>.node-content-wrapper>.expander-icon:before {
    content: '👋';
}

/* To add an icon */
.customise .sidebar .node_XXXXX>.node-wrapper>.node-content-wrapper>.expander-icon:before {
    content: "";
    background: url("YYYYY");
    background-size: 16px 16px;
    width: 16px;
    height: 16px;
}
{% /tab %}
{% /code %}