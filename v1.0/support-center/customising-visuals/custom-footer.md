---
type: page
title: Custom Footer
listed: true
slug: custom-footer
description: 
index_title: Custom Footer
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

Apply a custom footer to match your website.

Unlike [](/support-center/documentation-footer), this footer is placed outside of the documentation container and is written using HTML. Thus, the custom footer is a webpage itself with its own styles and scripts.

## How to set a custom footer

To customise footer:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the Sidebar.
- Under Customise, select Edit Footer {% icon classes="fas fa-code" /%}
- Enter the custom HTML, and select Done.
- Refresh the page to see the changes.

The custom HTML is contained in an iFrame. It should contain a head and body. We recommend that you link your website styles and scripts rather than writing them in the footer as this would allow your footer to be cached.

{% callout type="warning" title="Links" %}
If you have any links in the footer, make sure that you use `target="_parent"` to navigate inside the parent, not the iframe itself.
{% /callout %}

{% callout type="warning" title="Use Only HTTPS" %}
Load assets only from HTTPS sources, otherwise your readers will see a "Not Secure" badge next to the browser URL.
{% /callout %}