---
type: page
title: Landing Pages
listed: true
slug: landing-page
description: 
index_title: Landing Pages
hidden: 
keywords: 
tags: 
---

Help your readers find the resources they need right from Hello!

There are two types of Landing Pages:

- Main landing page: The page that lives at the root `/` of the docs site.
- Other landing pages: Pages that live on other paths. Other landing pages can be designated as 404 pages.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1554047902/-1/qt0rs0duol5a8fekpbed.png" mode="responsive" height="709" width="1035" %}
{% /image %}

## Main Landing Page

The main landing page is a modern smart entry point where your readers understand the contents of your developer hub. The main landing page lists the content of your project in a compact way in one page. The content is listed in a card format, where each card could link to a documentation or category, depending on the [structure](/support-center/landing-page#cards-generation-strategy) of your project.

## Main Landing Page Contents

Main landing page contains two main sections:

- **Hero**: Configurable title and a button that goes to the default page of your developer hub.
- **Cards**: An auto-generated list of cards that link to specific sections of your developer hub.

## Cards Generation Strategy

Cards are auto-generated according to the structure of your developer hub. The strategy for generating the cards is as such:

### Documentation

- If your developer hub contains multiple documentation, every documentation is contained in a card. Categories and pages are listed for every documentation in the card.
- If your developer hub contains one documentation, every category is contained in a card listing pages under it. If there are no categories, one card is listed having the pages.

## References

Every reference is contained in its own card.

## Customising Landing Page

Main landing page can be customised as such:

- **Hero background**: In your sidebar under Landing Page, you can choose a pattern for the background. The colour is the same as your [main colour](/support-center/customising-visuals#changing-colours).
- **Hero title**: The title can be changed directly from your Landing Page by editing it.
- **Hero button**: The button text can be changed by clicking on the button. You may also remove the button completely.

All landing pages can be enabled or disabled as needed from the sidebar as well.

Landing page META description can be modified from its settings.

Further customisation can be done using [Custom CSS](/support-center/custom-css) and [Custom Javascript](/support-center/custom-javascript) features.

## Custom Landing Page

If you want to use a custom landing page, writing your own HTML/CSS/JS, check [auto$](/support-center/custom-landing-page).

## Adding Landing Pages

To create a new landing page, at a path other than `/`, follow these steps:

1. From the sidebar, choose {% icon classes="fas fa-rocket inv-icon" /%} Landing Pages.
2. Click on {% icon classes="fas fa-plus" /%} Create new landing page.
3. Type in the path for the page to exist on (without basepath if any).
4. Click Save.
5. Customise it by clicking on Edit HTML.

## Removing Landing Pages

To remove a landing page, other than the main landing page, follow these steps:

1. From the sidebar, choose {% icon classes="fas fa-rocket inv-icon" /%} Landing Pages.
2. Choose the landing page you wish to delete.
3. Click on Delete at the top right.

## 404 Page

A landing page can be designated as a 404 page. When a reader visits an unrecognised URL, they would be taken to this 404 landing page. To designate a landing page as a 404 page:

1. From the sidebar, choose {% icon classes="fas fa-rocket inv-icon" /%} Landing Pages.
2. Choose the landing page you wish to designate.
3. Click on the settings {% icon classes="fas fa-cog" /%} 
4. Toggle Use as a 404 Page.

{% callout type="info" title="One 404 page" %}
Only one 404 page can exist in the project
{% /callout %}