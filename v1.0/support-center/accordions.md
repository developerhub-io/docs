---
type: page
title: Accordions
listed: true
slug: accordions
description: 
index_title: Accordions
hidden: 
keywords: 
tags: 
---

Accordions group content into collapsible titled sections, so readers can expand only the parts they need. They are handy for FAQs, optional details, and long reference material you want to keep tidy.

To create an accordion:

{% synced id="open-block-menu" /%}

- Select Accordion {% icon classes="fas fa-chevron-down" /%}

## Sections

An accordion starts with a single section. Use **Add section** to append another, and each section carries its own title and content.

A section can hold any other block: text, images, code blocks, callouts, and even a nested accordion.

## Fields

- **Title.** Every section has a title, shown on the header the reader clicks to expand or collapse the section.
- **Open.** Each section is collapsed when the page loads. Turn on a section's **Open** toggle to have it expanded by default instead.

## Example

{% accordion-group %}
{% accordion title="Getting started" %}
This section stays collapsed until the reader expands it.
{% /accordion %}

{% accordion title="Advanced features" open=true %}
This section is expanded by default because its **Open** toggle is on.

You can put other blocks inside an accordion section.
{% /accordion %}
{% /accordion-group %}
