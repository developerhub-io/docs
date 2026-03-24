---
type: page
title: Variables
listed: true
slug: variables
description: 
index_title: Variables
hidden: 
keywords: 
tags: inline-blocks
---

Project Variables help you label parts of your documentation that are repetitive, to be able to change them centrally in one place. It also allows you to [personalise](/support-center/personalised-docs) the documentation for your readers.

{% image url="https://image-archive.developerhub.io/image/upload/20816/ivlyuncbuan72p02gv9m/1570989659.png" mode="600" height="1360" width="1600" %}
{% /image %}

For example, you might want all of API reference to use the latest version in their example requests. Without variables, you would need to upload a new reference containing changes to each example request every time you update the version.

One of the example requests might look as such:

{% code %}
{% tab language="javascript" %}
var options = {
 "method": "GET",
 "url": "https://api.your-service.com/user",
 "body": {
   "version": "2019-10-12", // <-- change this to "%latest_version%"
   "id": 512
 }
};

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});
{% /tab %}
{% /code %}

With variables, you'll be able to centrally change version value, saving you time and effort.

## How to use Project Variables?

There are two things needed to get project variables setup:

- Add a JSON object of the variables that will be available in the documentation.
- Insert variable references in the documentation by wrapping it in percent signs as such `%variable%`.

## Where can you use Project Variables?

Project variables can be inserted in:

- Page content and blocks.
- API Reference descriptions.
- Index external links.
- [Custom javascript](/support-center/variables#using-project-variables-in-scripts).
- Default landing page layout.
- Custom HTML in landing pages.

## Editing Project Variables

To edit project variables, do the following:

- From the sidebar, select **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}
- Under **Project Variables**, click on the button on the right.
- Enter a JSON object defining all your variables. For example:

{% code %}
{% tab language="javascript" %}
{
  "project_name": "Xyz",
  "versions": {
    "latest_version": "1.54.2"
  }
}
{% /tab %}
{% /code %}

## Using Project Variables in References

To use project variables in an API Reference, replace all occurrences of the variable with the variable reference. For example, one definition property could be:

{% code %}
{% tab language="yaml" %}
version:
    type: string
    description: Version of the API
    example: "%versions.last_version%"
{% /tab %}
{% /code %}

Or to replace a variable named `subdomain` in the Server URL:

{% code %}
{% tab language="yaml" %}
servers:
  - url: https://{subdomain}.developerhub.io/api/v1
    variables:
      subdomain:
        default: "%subdomain%"
{% /tab %}
{% /code %}

{% callout type="warning" title="Warning" %}
Note that YAML requires you to use double quotations to escape a string containing percent sign.
{% /callout %}

## Using Project Variables in Scripts

To use project variables in [scripts](/support-center/custom-javascript), you must first set up the project to expose variables through `window.vars` object. To do that:

- From the sidebar, select **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}
- Under **Project Variables**, click on the button on the right.
- Check Expose Variables in Javascript.
- Click Save.

For the published docs, once the project loads, you'll be able to access the variables (defined under Project and injected through personalisation) through `window.vars`.

## Personalising Docs

You can use variables to personalise docs. Read more about it in [auto$](/support-center/personalised-docs).

### Known Limitations

- Variables do not work as HREFs for links.