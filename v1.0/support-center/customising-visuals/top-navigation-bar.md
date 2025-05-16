---
type: page
title: Top Navigation Bar
listed: true
slug: top-navigation-bar
description: 
index_title: Top Navigation Bar
hidden: 
keywords: 
tags: customisation
---

The top navigation bar can be customised in multiple ways:

- [Logo](/support-center/customising-visuals#changing-logo)
- Bar colour ([brand colour](/support-center/customising-visuals#changing-colours)) and navigation links colour
- [Links](/support-center/top-navigation-bar#adding-links--home-button)
- [Stickiness](/support-center/top-navigation-bar#sticky-top-navigation-bar)
- [Navigation Structure](/support-center/top-navigation-bar#navigation-structure)

## Navigation Structure

By default, the top navigation hosts a list of tabs. Starting with the Home tab which goes to the landing page, and then a tab for every documentation section and API reference.

The navigation structure can be further customised to feature navigation groups; a way for multiple documentation sections and API references to be grouped together under a dropdown.

{% video videoId="https://uploads.developerhub.io/prod/02/hi6hcqh51jcdoterj0alxqwd79v6pu56w0ni4f2j4x69193gtfc3u7im5dmvu0f0.mp4?controls=0&autoplay=1&loop=1&muted=1&playsinline=1" provider="raw" %}
{% /video %}

To use navigation groups, first they need to be created. Then, documentation sections and API references can be assigned to navigation groups.

To create a navigation group:

1. Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Navigation Groups, click "Create navigation group".
3. Give it a title and click Create.

You can reorder the navigation groups as needed here.

Now to assign a documentation section or an API reference to the navigation group:

1. From the sidebar, choose Documentation or API Reference.
2. Open the settings by clicking on the settings {% icon classes="fas fa-cog" /%} icon.
3. Next to Navigation Group, assign a navigation group.

{% callout type="info" title="Info" %}
If a documentation section or an API reference is not assigned to a navigation group, it will show up at the end of the tab list. If you wish for the documentation section or API reference to show up in a different order, create a navigation group and assign the documentation section or API reference to it. If a navigation group only contains one documentation section or API reference, it will show as a link tab, not as a dropdown.
{% /callout %}

## Adding Links / Home Button

The logo, and four top navigation links can be setup for external linking to another website, or internal linking inside the documentation. To setup the navigations links:

1. Hover over the top navigation and click on Edit Navigation {% icon classes="fas fa-edit" /%} in the top left corner.
2. Type in the title.
3. Type in the link.
4. Click outside the window to close the top navigation editor and save.

You can change if links open in a new tab or the same tab by checking **Open Links in New Tab**.

The last two links only show in documentations that have wide layout.

{% callout type="info" title="Go Home" %}
Setting the link to `/` goes to the landing page, or the default page if no landing page is setup.
{% /callout %}

{% callout type="warning" title="Automatic Saving" %}
Navigation links will be automatically saved on change without prompt
{% /callout %}

## Sticky Top Navigation Bar

To set the top navigation bar to stick to the top when page is scrolled:

1. Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Customisation, check "Is Top Navigation Bar Sticky?"

The setting will be saved immediately.