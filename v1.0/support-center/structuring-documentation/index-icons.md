---
type: page
title: Index Icons
listed: true
description: 
index_title: Index Icons
hidden: false
keywords: 
tags: 
---

You can give any element in your documentation index an icon, and your readers see it next to that entry in the navigation sidebar. Icons work well as landmarks for the few entries readers look for most, such as a quick start, a changelog, or a link out to your status page.

## Adding an Icon

- In the documentation index, hover the entry and click on the menu icon {% icon classes="fas fa-ellipsis-v" /%} next to it.
- Select **Add Icon** {% icon classes="fas fa-icons" /%}. If the entry already has one, the item reads **Change Icon**.
- Choose an icon, then click **Save**.

Pages, categories, labels, and [external links](external-links.md) can all carry an icon. Separators cannot.

{% callout title="Who can set icons" %}
Setting an icon is available to admins and publishers. Writers and reviewers do not see the menu item.
{% /callout %}

## Choosing an Icon

The dialog offers two sources, and an entry uses one or the other. Picking from the icon set replaces an uploaded image, and uploading an image replaces a picked icon.

### Font Awesome

Search the built-in set under **Choose an icon**, or browse the results grid. The tabs across the top switch between the **Solid**, **Regular**, and **Brands** styles.

%product% loads Font Awesome 7 Free, which is 2,157 icons across those three styles. The Pro styles (Light, Thin, Duotone, and Sharp) are not included. To browse the same set visually before you search, use [Font Awesome's own search](https://fontawesome.com/search?ic=free) with the Free filter on.

Searching understands the older Font Awesome 5 names too, so typing `times`, `cog`, or `search` still finds `xmark`, `gear`, and `magnifying-glass`.

### Uploading an Image

Click **Upload an image** to use your own artwork instead, which is the way to put a product or partner logo in the index. Use a square SVG or PNG of at least 32×32, since the icon renders at 15×15 next to the entry title. Uploaded images keep their own colours and are never tinted.

## Removing an Icon

Open the menu icon {% icon classes="fas fa-ellipsis-v" /%} next to the entry, select **Change Icon**, click **Remove**, then **Save**.

## How Icons Affect the Index

Icons are designed to be used sparingly, so the index stays readable when only a few entries carry one.

As soon as one entry has an icon, a narrow slot is reserved for it on every entry in that documentation, and titles line up along a single edge. Entries with no icon leave the slot empty rather than showing a placeholder, which is what lets the icons you did set stand out. Categories reserve their slot separately, so giving your pages icons does not shift your category headings.

If you remove the last icon in a documentation, the slot disappears and the index returns to its previous layout.

## Icons in a Synced Repository

In a [GitHub-synced](../github-sync.md) project, icons live in the documentation's `_nav.yaml`, not in page frontmatter. The `icon` key sits beside the entry's own key:

{% code %}
```yaml {% title="_nav.yaml" %}
items:
  - introduction
  - page: authentication
    icon: key
  - page: parent
    icon: book-open
    items:
      - parent/child
  - category: Guides
    icon: 'https://assets.example.com/guides.svg'
  - label: Extras
    icon: tag
  - link:
      title: Status
      url: 'https://status.example.com'
    icon: heartbeat
  - separator
```
{% /code %}

Write the value in one of these forms:

- **Solid**: the icon name on its own, such as `rocket`. There is no `fas:` prefix; solid is the default style.
- **Regular**: prefix with `far:`, such as `far:bell`.
- **Brands**: prefix with `fab:`, such as `fab:github`.
- **An image**: the full `https://` URL of the image. Relative paths and protocol-relative URLs are not accepted.

A page normally appears in `_nav.yaml` as a bare path such as `- introduction`. It expands to the `page:` form only when it carries an icon, so adding this feature does not rewrite the navigation of repositories that use no icons.

For a link entry, note that `icon` is a sibling of `link`, not one of the fields inside it.

Your repository is the source of truth for icons, as it is for the rest of your navigation. Deleting an `icon` line removes the icon from that entry on the next sync.

{% callout type="warning" title="Icon names are not checked" %}
An icon name that does not exist in Font Awesome 7 Free, including a Pro-only name, is still accepted. It syncs without a warning and then renders as an empty slot in the index. If an icon does not appear, check the name against the [Free set](https://fontawesome.com/search?ic=free) first.

A value that is neither a valid name nor an image URL, such as a raw class like `fas fa-key`, is reported by the sync and ignored.
{% /callout %}

{% callout title="Writing navigation with an AI agent" %}
The `organize-docs-repo` [Agent Skill](../github-sync/write-markdoc-with-ai.md) ships the full list of valid icon names, so an agent editing your `_nav.yaml` picks real ones instead of guessing.
{% /callout %}

Icons set on a page are carried over when you duplicate the page or clone the version.

{% callout title="Inline icons in a page" %}
To put an icon inside the body of a page rather than in the index, see [Icons](../icons.md).
{% /callout %}
