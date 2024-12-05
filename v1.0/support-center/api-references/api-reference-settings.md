---
type: page
title: API Reference Settings
listed: true
slug: api-reference-settings
description: 
index_title: API Reference Settings
hidden: 
keywords: 
tags: 
---

Along with [code generation](/support-center/code-generation), each API Reference has settings which you can manage. You can access the settings by click on Settings {% icon classes="fas fa-cog" /%} from the sidebar &gt; Reference.

{% image url="https://uploads.developerhub.io/prod/02/0hjexvjnju890j1pv3hw34iec82jwf8alpp23y84p8pj45hlel9dv39z6lez3k7y.png" mode="responsive" height="529" width="446" %}
{% /image %}

## Allow Download

Allow Download setting allows the API Reference to be downloadable by showing a button at the top of the page.

## Show Try It Out

Enables [auto$](/support-center/try-it-out) to test APIs right from the API Reference.

## Show Content-Type Header

For operations (OAS3 only) that have request body, checking this option shows a header in the example defining the content-type. For example:

{% code %}
{% tab language="bash" %}
curl --request POST \
 --url https://api.developerhub.io/api/v1/version/{versionId}/reference \
 --header "Content-Type: application/json" # <--- This line would be added 
 --form "file=@{file}"
{% /tab %}
{% /code %}

## Show Accept Header

For operations (OAS3 only), checking this options shows a header in the example defining the accepted response media type. For example:

{% code %}
{% tab language="bash" %}
curl --request GET \
 --url https://api.developerhub.io/api/v1/page?version_id={version_id}&version_slug={version_slug}&documentation_id={documentation_id}&documentation_slug={documentation_slug}&page_slug={page_slug}&format={format} \
 --header "Accept: application/json"
{% /tab %}
{% /code %}

## Allow Tags to be Expand

If your API Reference is dense, loading thousands of items could be slow. To optimise for performance, you can check this option to allow tags to expand. By allowing tags to expand, you can load an API Reference of any size without performance hit.

When tags are allowed to expand, the tag with its description would show, alongside an table of all the operations available under this tag. Also, a button to "Show" the operations will appear.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1612663200/v2_1/zw6p9hmb6rhrzfgiznpf.png" mode="responsive" height="489" width="1410" %}
{% /image %}

## Allow Index to Collapse

When checked, the tags in the index are collapsible.

## Show Request Example Code Samples

Checked by default, when unchecked, would only show an example URL or request body instead of allowing the reader to pick a code library to see a code sample.