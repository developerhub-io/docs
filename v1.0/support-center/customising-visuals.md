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

{% image url="../../assets/customisation-brand-assets.png" /%}

## Custom CSS and Footer

Check [Custom CSS](customising-visuals/custom-css.md), and [Custom Footer](customising-visuals/custom-footer.md) pages.

## Changing Logo

To change the logo:

1. Open Project Settings → **Customisation**.
2. In the Brand assets card, click **Upload logo** next to Logo.
3. Choose the new logo.

Matcha's transparent top bar shows your logo on the page colour, which is near-black in dark mode. If your logo does not read on dark, click **Upload logo** next to **Logo for dark backgrounds** and choose a version for dark mode. Left empty, the regular logo is used in both modes.

You can also change [the URL](customising-visuals.md#adding-links--home-button) which is navigated to when the logo is clicked on.

{% callout title="Logo" %}
It is best to have a wide logo with transparent background.
{% /callout %}

To change the website icon (favicon):

1. Open Project Settings → **Customisation**.
2. In the Brand assets card, click **Upload favicon** next to Favicon.
3. Choose the new favicon.

{% callout title="Favicon" %}
We automatically rescale your favicon if it was too big. Note that the favicon only shows on live mode, and not in the editing mode.
{% /callout %}

{% callout type="warning" title="Automatic Saving" %}
Logos and favicon are saved automatically on change without prompt.
{% /callout %}

## Changing UI

%product% provides three UIs: Original, Next and Matcha.

### Original UI

Original UI is the first UI of %product%, notable for its hovering search bar. The different sections and version are hidden behind dropdown, and the index has coloured categories.

{% image url="../../assets/reader-ui-original.png" /%}

### Next UI

Next UI is the new UI. Next UI features a sleek design where different sections are visible in the top navigation, and a redesigned index with clearer margins and animation. It also providers a better [search experience](using-search.md#next-ui-search).

{% image url="../../assets/reader-ui-next.png" /%}

### Matcha UI

Matcha is Next restyled, with a one-row top bar and a tree index. Unless you have chosen a [font](customising-visuals.md#changing-font), it uses IBM Plex Sans. New projects start on Matcha.

{% image url="../../assets/matcha-ui.png" /%}

#### Transparent Top Bar

On Matcha, the top bar can take the page colour (white in light mode, near-black in dark) instead of your header colour:

1. Open Project Settings → **Customisation**.
2. In the Colour \& typography card, switch on **Transparent top bar**.
3. Click **Save changes** in the top menu.

Give it a [logo for dark backgrounds](customising-visuals.md#changing-logo) so your logo still reads in dark mode.

### Choosing a UI

To change the UI:

1. Open Project Settings → **Customisation**.
2. In the Look and feel card, under **UI version**, choose **Original**, **Next** or **Matcha**.
3. Click **Save changes** in the top menu.

{% callout title="Custom CSS" %}
If you have [custom CSS](customising-visuals/custom-css.md), check it against the new UI before switching. Add `?ui=3` to the address of any page of your published docs to see it in Matcha (`?ui=2` for Next), without changing anything for your readers.
{% /callout %}

{% callout title="Navigation bar sections" %}
In Next and Matcha, the different sections are laid out in the top navigation bar. On Matcha, sections that do not fit move into a **More** menu at the end of the bar. In mobile layout, they collapse into a section picker dropdown.
{% /callout %}

## Removing %product% Branding

Published documentation carries the %product% name: a **Powered by %product%** credit at the foot of each page, or a logo under the index on the free plan. You can publish without it:

1. Open Project Settings → **Customisation**.
2. In the Look and feel card, switch on **Remove %product% branding**.
3. Click **Save changes** in the top menu.

{% image url="../../assets/remove-developerhub-branding.png" %}
Project Settings → Customisation → Look and feel
{% /image %}

{% callout title="Paid Plan" %}
Removing the branding needs a plan that includes it. See [Pricing](https://developerhub.io/pricing).
{% /callout %}

## Changing Colours

The header, link and navigation colours are modifiable. To change the colours:

1. Open Project Settings → **Customisation**.
2. In the Colour \& typography card, click the swatch next to the colour you want to change.
3. Pick the desired colour. We will warn you if the colour is not contrasting enough. The change previews live in the embedded reader preview at the top of the pane.
4. Click **Save changes** in the top menu.

{% image url="../../assets/customisation-colour-picker.png" /%}

{% callout title="Link Colour" %}
Make sure to set the link colour distinct from the font colour. This is usually your secondary brand colour. The text in your pages is almost black in light theme (white in dark theme), so you need a colourful link for it to be distinguished.
{% /callout %}

## Changing Font

To change the font of the entire project:

1. Open Project Settings → **Customisation**.
2. In the Colour \& typography card, click the Font row.
3. Choose from the list of Google Fonts available. The font is previewed immediately in the current documentation and the embedded reader preview at the top of the pane.
4. Click **Save changes** in the top menu.

{% image url="../../assets/customisation-font-picker.png" /%}

{% callout title="Paid Plan" %}
Changing font is only a paid plan feature
{% /callout %}

{% accordion-group %}
{% accordion title="Not using Google Fonts?" %}
If you are not using Google Fonts, you can serve your own font to your documentation portal as described in our own blog post: [Using your own Custom Font](https://developerhub.io/blog/using-your-own-font/)
{% /accordion %}

{% accordion title="Font Weights Missing?" %}
If the font you are using does not have all the font weights we expect, then you can change the actual font weight for an expected one. See [Font Weights](customising-visuals/custom-css.md#font-weights).
{% /accordion %}
{% /accordion-group %}

## Need More Customisation?

Check also our [popular customisations](css-customisations.md).

[Let us know](contact-us.md) what you need, we'd love to help!
