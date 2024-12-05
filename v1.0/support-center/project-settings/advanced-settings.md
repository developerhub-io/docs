---
type: page
title: Advanced Settings
listed: true
slug: advanced-settings
description: 
index_title: Advanced Settings
hidden: 
keywords: 
tags: 
---

## Ask before Publishing

To publish safely ensuring all comments have been resolved, you can check the Ask Before Publishing setting. To do that:

- Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- At the bottom under Advanced Settings, check Ask Before Publishing.

## Lock Page when Editing

To ensure only one user is editing the page at a time, you can check the Lock Page when Editing setting. To do that:

- Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- At the bottom under Advanced Settings, check Lock Page when Editing.

When this setting is enabled and a user is editing, all other users will see a banner informing them that the page is locked. While this banner is showing, they will not be able to modify the page until the editing user saves or discards. Once the page gets unlocked, the page will refresh automatically.

## Require Annotating on Saving

Force editors to annotate the changes to be saved. This helps you keep a clean history. To do that:

- Click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- At the bottom under Advanced Settings, check Require Annotating on Saving.

## Other Settings

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

For advanced settings that we do not provide through the UI, they can modified through [auto$](/support-center/custom-javascript).

The available settings are (with their defaults):

{% code %}
{% tab language="javascript" %}
{
  warnings: {
    oldVersion: false // false|true: Show a banner when viewing an older version
  },
  index: {
    categoryToggle: false // false|true: Set true to disable automatic category toggling on changing page
  },
  search: {
    scope: "version" // "version"|"section": Set the scope of the search bar
  },
  tableOfContents: {
    hideH3: false, // false|true: Hides H3 from table of contents
    hideH4: false, // false|true: Hides H4 from table of contents. Has no effect if hideH3 is enabled.
    highlightActive: true // false|true: Highlights last scrolled to heading in table of contents
  },
  code: {
    theme: "monokai", // Any theme from https://codemirror.net/demo/theme.html (must import CSS as well): Sets the theme for code blocks
    githubTheme: "github", // Any theme from https://emgithub.com/: Sets the theme for GitHub Code blocks
    showLineNumbers: false // false|true: Shows a gutter with line numbers in code blocks
  },
  seo: {
    titleFormats: { // Modifies the browser tab title + META title. Use %page%, %section%, %version% and %project% as placeholders.
      page: '%page% - %project%',
      documentation: '%section% - %project%',
      reference: '%section% - %project%',
      landingPage: '%project%'
    },
  },
  apiReference: {
    collapsedMaxHeight: 1024 // Height which if exceeded the expand button shows for tables/examples
  },
  scrolling: { // Only apply this if using Original UI or if you modified the height of the top navbar 
    scrollTopOffsetOnFragmentChange: { // If top navbar is set to sticky, modify the values below to ensure that headings show below the topnav
      documentation: 0, // -90 is recommended if navbar height is not changed
      apiReference: 0 // -50 is recommended if navbar height is not changed
    }
  },
  feedback: {
    disable: false // Disables feedback control in runtime
  }
}
{% /tab %}
{% /code %}

## Applying Settings

To change a setting, use the `apply`  function on `window.settings`:

{% code %}
{% tab language="javascript" %}
<script>
  window.settings.apply({
  	index: {
      categoryToggle: true
    },
    search: {
      scope: "section"
    }
  });
</script>
{% /tab %}
{% /code %}