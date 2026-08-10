---
type: page
title: Top Navigation Bar
listed: true
description: 
index_title: Top Navigation Bar
hidden: false
keywords: 
tags: customisation
---

The top navigation bar can be customised in multiple ways:

- [Logo](../customising-visuals.md#changing-logo)
- Bar colour ([brand colour](../customising-visuals.md#changing-colours)) and navigation links colour
- [Links](top-navigation-bar.md#adding-links--home-button)
- [Stickiness](top-navigation-bar.md#sticky-top-navigation-bar)
- [Navigation Structure](top-navigation-bar.md#navigation-structure)

## Navigation Structure

By default, the top navigation hosts a list of tabs. Starting with the Home tab which goes to the landing page, and then a tab for every documentation section and API reference.

The navigation structure can be further customised to feature navigation groups; a way for multiple documentation sections and API references to be grouped together under a dropdown.

{% video provider="raw" videoId="https://uploads.developerhub.io/prod/02/nrz4mx3xlcly8g3w4amahs5n7a68nudf2ln5h4jaibjnilq6qhu89y3zseojqeu3.mp4?controls=0&autoplay=1&loop=1&muted=1&playsinline=1" /%}

To use navigation groups, first they need to be created. Then, documentation sections, API references, and changelogs can be assigned to navigation groups.

To create a navigation group:

1. Open Project Settings → **Content** → **Navigation Groups**.
2. Click **Create group**.
3. Give it a title and click **Create**.

You can reorder the navigation groups as needed here, by dragging them. The order applies across every version. A **Reader preview** above the list renders the top navigation live as your readers will see it.

Now to assign a documentation section or an API reference to the navigation group:

1. Open Manage Sections (section menu → settings {% icon classes="fas fa-cog" /%} cog).
2. Select the documentation or API reference.
3. Next to Navigation Group, assign a navigation group.

To assign a [changelog](../changelogs.md) instead, open Manage Changelogs, select the changelog, and pick a group next to **Navigation group**. Choose **None** to take it back out. A changelog can belong to one group at a time.

### Navigation Group Icons

A navigation group can carry an icon, shown beside its label in the top navigation bar and in the navigation picker on mobile.

{% image url="../../../assets/navigation-group-icons.png" /%}

To set one, open Project Settings → **Content** → **Navigation Groups** and click **Add group icon** in the group's Actions column (it reads **Change group icon** once one is set). The picker is the same one used for [sidebar icons](../structuring-documentation/index-icons.md), so you can choose a Font Awesome icon or upload your own image.

{% callout title="Info" %}
If a documentation section or an API reference is not assigned to a navigation group, it will show up at the end of the tab list. If you wish for the documentation section or API reference to show up in a different order, create a navigation group and assign the documentation section or API reference to it. If a navigation group only contains one documentation section or API reference, it will show as a link tab, not as a dropdown.
{% /callout %}

## Adding Links / Home Button

The logo, and four top navigation links can be setup for external linking to another website, or internal linking inside the documentation. To setup the navigation links:

1. Open Project Settings → **Customisation**.
2. In the Top navigation links card, type the title and link for each of the four slots.
3. Use the **Open links in new tab** toggle to choose whether links open in a new tab.
4. Click **Save changes** in the top menu.

The last two links only show in documentations that have wide layout.

{% callout title="Go Home" %}
Setting the link to `/` goes to the landing page, or the default page if no landing page is setup.
{% /callout %}

## Sticky Top Navigation Bar

To set the top navigation bar to stick to the top when page is scrolled:

1. Open Project Settings → **Customisation**.
2. Check **Is top navigation bar sticky?**.
3. Click **Save changes** in the top menu.
