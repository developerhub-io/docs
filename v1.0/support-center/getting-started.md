---
type: page
title: Getting Started
listed: true
description: 
index_title: Getting Started
hidden: false
keywords: 
tags: 
---

{% html %}
<div style="text-align: center;">
	<img id="dhImage" style="max-width: 300px;" />
</div>
{% /html %}

{% p /%}

Welcome %user.name% to our *Supercharged* documentation which has been written using %product%.

Learn how to use %product% in our step-by-step guide:

{% html %}
<!--ARCADE EMBED START-->
  <iframe src="https://demo.arcade.software/mXfTOZfQRMMXPJIqWjzp?embed&embed_mobile=tab&embed_desktop=tab&show_copy_link=true" 
          title="How to Edit and Publish Updates in DeveloperHub Documentation" 
          frameborder="0" loading="lazy" 
          webkitallowfullscreen mozallowfullscreen allowfullscreen 
          allow="clipboard-write" style="top: 0; left: 0; width: 100%; height: 500px; color-scheme: light;" 
          onload="window.postMessage('resize', '*')" ></iframe>
{% /html %}

## What is %product%?

%product% is an agentic documentation platform. You write product \& user guides, developer hubs/portals, knowledge bases and support centres, and an agent helps you keep them level with your product.

Attach your code repository and the agent reads the pull requests your team opens, works out which pages they make wrong, and stages the edits for someone to review. Nothing publishes on its own. See [Self-Updating Docs](self-updating-docs.md).

You can also just ask our AI Agent. One request can restructure a section, rename a parameter across pages and API references, or turn your [search analytics](search-analytics.md) into the pages your readers could not find. See [AI Agent](ai-agent.md).

Everything else is managed for you. No designing, no infrastructure to run, no software team to hire.

## Why should I use %product%?

Both halves of your team work on the same pages, the way they already work. Writers get an editor where what you are editing looks like what publishes, with no MDX, YAML or frontmatter to learn. Developers keep docs-as-code, with [two-way GitHub sync](github-sync.md) and an [Editor MCP server](ai-features/mcp-server/editor-mcp-server.md) for Claude Code, Cursor or Codex.

And there is a lot more besides 💛

- A design your readers can navigate, so your docs answer them instead of sending them to support 📈
- Format with a [toolbar](writing-documentation/formatting-text.md), [keyboard shortcuts](keyboard-shortcuts.md) or [Markdown](writing-documentation/using-markdown.md), whether or not your writers are technical 👩‍💻
- A review process, with [permissions](collaboration.md), [comments](comments.md) and [drafts](writing-documentation/draft-mode.md).
- AI for your readers: an [AI Assistant](writing-documentation/ai-search.md) that answers from your pages and links where it got the answer, plus a [Reader MCP server](ai-features/mcp-server/reader-mcp-server.md), [llms.txt](ai-features/llms-txt.md) and a Markdown copy of every page, so their own assistants quote your docs instead of guessing {% icon classes="fas fa-robot" /%}
- AI in the editor: [AI Writing Tools](writing-documentation/ai-writer.md) and a [META descriptions generator](ai-features/ai-summarisation.md).
- [Analytics](integrations/google-analytics.md), [search](using-search.md), [search analytics](search-analytics.md), [SEO](seo.md), [link checking](writing-documentation/page-linking.md#listing-broken-links), [glossary](glossary.md) and [feedback](feedback.md), all built in (seriously) 🚀
- [Host](hosting.md) on your [own domain](hosting/using-custom-domain.md), a [path on your site](hosting.md#hosting-under-an-existing-website), or a [subdomain](hosting.md#hosting-under-product-subdomain) of ours 🔗
- Native [OpenAPI 2 through to 3.2](api-references.md), with an API editor and playground built in, so your API reference sits beside your guides 🗂
- Change the look completely with [custom CSS](customising-visuals/custom-css.md) and [JavaScript](custom-javascript.md).

Explore more below:

{% cards %}
{% card title="First Steps" text="Sign up, create your project and publish your first page" link="getting-started/first-steps.md" /%}
{% card title="Importing Documentation" text="Bring your existing docs across from your current tool" link="importing-documentation.md" /%}
{% card title="Formatting Text" text="Toolbar, Markdown and keyboard shortcuts" link="writing-documentation/formatting-text.md" /%}
{% card title="Blocks" text="Callouts, tabs, code, images, tables and more" link="writing-documentation/blocks.md" /%}
{% card title="API References" text="OpenAPI viewer, visual editor and API playground" link="api-references.md" /%}
{% card title="Collaboration" text="Roles, comments, drafts and the review flow" link="collaboration.md" /%}
{% card title="AI Agent" text="Ask for a change in a conversation and review what it drafts" link="ai-agent.md" /%}
{% card title="AI Features" text="AI Writing Tools, AI Assistant, MCP servers and AI credits" link="ai-features.md" /%}
{% card title="GitHub Sync" text="Two-way sync, so your docs live in your repository too" link="github-sync.md" /%}
{% card title="Hosting" text="Your own domain, a subdomain of ours, or a path on your site" link="hosting.md" /%}
{% card title="Customisation" text="Logo, favicon, colours, fonts and custom CSS" link="customising-visuals.md" /%}
{% card title="Conditional Content" text="Show different content to different audiences" link="conditional-content.md" /%}
{% /cards %}

---

We have been building %product% since December 2017, to make writing documentation something your team enjoys rather than something it works around.
