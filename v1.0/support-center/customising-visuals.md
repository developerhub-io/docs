---
type: page
title: Customising Visuals
listed: true
description: 
index_title: Customising Visuals
hidden: false
keywords: white-labelled, white-label, whitelabel, whitelabelling
tags: customisation
---

%product% supports the following customisations: [UI](customising-visuals.md#changing-ui) , [CSS](customising-visuals/custom-css.md), [Footer](customising-visuals/custom-footer.md), [theme (dark mode)](customising-visuals/theme.md), [code theme](customising-visuals/code-theme.md), logos, header colour, link colour, font and navigation links.

{% image url="https://uploads.developerhub.io/prod/02/4xxcn5idwk0zimsk1iyxiw10mvrusone25kd7etmqf0irl8b9yx0phjwnyzcz8fw.png" width=276 /%}

## Custom CSS and Footer

Check [Custom CSS](customising-visuals/custom-css.md), and [Custom Footer](customising-visuals/custom-footer.md) pages.

## Changing Logo

To change the logo:

1. Open Project Settings → **Customisation**.
2. In the Brand assets card, click **Change** next to Logo.
3. Choose the new logo.

You can also change [the URL](customising-visuals.md#adding-links--home-button) which is navigated to when the logo is clicked on.

{% callout title="Logo" %}
It is best to have a wide logo with transparent background.
{% /callout %}

To change the website icon (favicon):

1. Open Project Settings → **Customisation**.
2. In the Brand assets card, click **Change** next to Favicon.
3. Choose the new favicon.

{% callout title="Favicon" %}
We automatically rescale your favicon if it was too big. Note that the favicon only shows on live mode, and not in the editing mode.
{% /callout %}

{% callout type="warning" title="Automatic Saving" %}
Logo and favicon are saved automatically on change without prompt.
{% /callout %}

## Changing UI

%product% provides two UIs, %product% Original and %product% Next.

### Original UI

Original UI is the first UI of %product%, notable for its hovering search bar. The different sections and version are hidden behind dropdown, and the index has coloured categories.

{% image url="https://uploads.developerhub.io/prod/02/1i99io8bxcrui9rkvtdpxgnnop4h4umjxi03lb6l4ujz27znuulsxbdrmkcr7g0v.png" /%}

### Next UI

Next UI is the new UI. Next UI features a sleek design where different sections are visible in the top navigation, and a redesigned index with clearer margins and animation. It also providers a better [search experience](using-search.md#next-ui-search).

{% image url="https://uploads.developerhub.io/prod/02/gisilvod2lm55ppsfekwri28qjfpk1deoc98ftqniqtb3juejaflqbidqhcf2ao1.png" /%}

To change the UI:

1. Open Project Settings → **Customisation**.
2. In the Customisation card, choose which UI to use.
3. Click **Save changes** in the top menu.

{% callout title="Navigation bar sections" %}
In Next UI, the different sections are laid out in the top navigation bar. In mobile layout, they would collapse into a section picker dropdown.
{% /callout %}

## Changing Colours

The header, link and navigation colours are modifiable. To change the colours:

1. Open Project Settings → **Customisation**.
2. In the Colour \& typography card, click the swatch next to the colour you want to change.
3. Pick the desired colour. We will warn you if the colour is not contrasting enough. The change previews live in the embedded reader preview at the top of the pane.
4. Click **Save changes** in the top menu.

{% image url="https://uploads.developerhub.io/prod/02/t5tfi5ko1eerfgdi92b3qkk5m6mnshfaktg43nvnfudtlhvr8hvji926ke7hvscs.png" width=372 /%}

{% callout title="Link Colour" %}
Make sure to set the link colour distinct from the font colour. This is usually your secondary brand colour. The text in your pages is almost black in light theme (white in dark theme), so you need a colourful link for it to be distinguished.
{% /callout %}

## Changing Font

To change the font of the entire project:

1. Open Project Settings → **Customisation**.
2. In the Colour \& typography card, click the Font row.
3. Choose from the list of Google Fonts available. The font is previewed immediately in the current documentation and the embedded reader preview at the top of the pane.
4. Click **Save changes** in the top menu.

{% image url="https://uploads.developerhub.io/prod/02/a42me6zj2gppl815wkrthfxrbbk56pfb6k3s7jk9h0zqmi8e7xbhhqm4395lqcb3.png" /%}

{% callout title="Paid Plan" %}
Changing font is only a paid plan feature
{% /callout %}

### Not using Google Fonts?

If you are not using Google Fonts, you can serve your own font to your documentation portal as described in our own blog post: [Using your own Custom Font](https://developerhub.io/blog/using-your-own-font/)

### Font Weights Missing?

If the font you are using does not have all the font weights we expect, then you can change the actual font weight for an expected one. See [Font Weights](customising-visuals/custom-css.md#font-weights).

## Need More Customisation?

Check also our [popular customisations](css-customisations.md).

[Let us know](contact-us.md) what you need, we'd love to help!
