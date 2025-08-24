---
type: page
title: URL Redirects
listed: true
slug: url-redirects
description: 
index_title: URL Redirects
hidden: 
keywords: 
tags: 
---

You may need to set up URL redirects if you:

- Moved from a different platform that had different URL structures.
- Changed a page slug and it is already linked externally outside of %product%.
- For search engine optimisation.

## How to set up URL redirects?

URL redirects are server-based, 301 permanent redirects. 301 redirects are followed by robots and search engines.

To set up URL redirects:

- From the sidebar, click on Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Hosting, click on Edit Redirects {% icon classes="fas fa-random" /%}.
- Add the redirection rules as follows:
    - Every rule is on a line. Rules take precedence by order.
    - Every rule has a pattern, and a destination, separated by `>>` (exactly: a space, two angle brackets, a space).
    - The pattern is regex-based, such as: `/android-sdk/intro` or `/ios-sdk/(.*)`.
    - The destination is regex as well and can have replacements, such as: `/android-sdk/getting-started` or `/ios-sdk/$1`.
    - Do not include URL origin or project basepath.
    - Leave no empty lines. Do not add comments.
    - Any invalid rule will be stripped upon saving.
    - Do not add the project basepath in the pattern or destination.
    - Redirection rules are evaluated from first to last. Only the first one matching is used for redirection.
    - Once a redirection rule matches, a **regex replace** happens. Thus if a rule is `ios >> android`, then for every `ios` that exists in the path, it is replaced into `android`. To do an exact match, use `^` to denote the start of the path and `$` to denote the end of the path, such as: `^/android-sdk/intro$ >> /ios-sdk/intro`.

- Hit Save.

It may take up to 5 minutes for changes to take effect.

{% callout type="warning" title="Note" %}
Redirected URLs will not redirect again. If you have a rule that redirects URL X to URL Y, and then another rule that redirects URL Y to URL Z, then only the first redirection will be processed. The user will end up on URL Y.
{% /callout %}

{% callout type="info" title="Regex Replacements" %}
Under the hood, all rules are regex based. For exact matches, you might want to add `$` to the end of the pattern. `$` in regex denotes end of string.

For example, if you wish to redirect `/docs/help` but not `/docs/help-and-support`, you must use the pattern `/docs/help$`.
{% /callout %}

If you need redirections to work within the single-page application, then look at [JS redirection rules](/support-center/custom-javascript#redirection-rules).

## Scope of Redirects

URL redirects work within the scope of a project. They cannot redirect to another site or another project.

For example, for a project hosted at `https://docs.pied-piper.com`, a redirect rule could redirect `https://docs.pied-piper.com/doc/page` to `https://docs.pied-piper.com/doc2/page2`, but it cannot redirect to `https://docs.other-site.com/doc/page`.

If you wish to have complete site redirect, please [contact us](/support-center/contact-us).

## Redirection Examples

1. To redirect from `/android-sdk/intro`  to `/android-sdk/getting-started`

{% code %}
{% tab language="none" title="Redirects" %}
^/android-sdk/intro$ >> /android-sdk/getting-started
{% /tab %}
{% /code %}

2. To redirect from `/android-sdk/<any>` to `/ios-sdk/<any>`.

{% code %}
{% tab language="bash" title="Redirects" %}
^/android-sdk/(.*) >> /ios-sdk/$1
{% /tab %}
{% /code %}