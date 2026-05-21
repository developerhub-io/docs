---
type: page
title: Managing API References
listed: true
slug: managing-api-references
description: 
index_title: Managing API References
hidden: 
keywords: 
tags: 
---

%product% generates beautiful and powerful API References from your API specification files. See our [Swagger Petstore](https://swagger.developerhub.io/v1.0/swagger-petstore/ref) demo here.

See [Uploading References](/support-center/uploading-references) to learn how to add an API reference to your version.

## Manage Sections

API references and documentation sections live on the same **Manage Sections** page. To open it:

- In the editor top navigation, click on the section menu.
- Click the settings {% icon classes="fas fa-cog" /%} cog.

The left list groups sections under **Documentation** and **API Reference** headers. Select an API reference to see and edit its settings on the right.

## Creating API References

To create an API reference:

1. Open the section menu in the top navigation.
2. Under the API Reference group, click **+ New API reference**.
3. Choose one:
    - **Create from scratch** — start with an empty OpenAPI definition.
    - **Upload OpenAPI definition** — upload an existing file. See [Uploading References](/support-center/uploading-references).
    - **Merge references** — combine two or more existing references. See [Merging API Definitions](/support-center/merge-api-definitions).

## Deleting API References

To delete an API reference:

- Open Manage Sections.
- Select the API reference.
- In the Danger zone card, click **Delete section**.
- Confirm your deletion.

{% callout type="warning" title="Warning" %}
Once an API reference is deleted, it cannot be retrieved back.
{% /callout %}

## Ordering API References

To change an API reference order in the picker:

- Open Manage Sections.
- Drag the reference in the left list from the handle {% icon classes="fas fa-grip-vertical" /%}.
- Drop the reference in the desired place.

You can only reorder within the API Reference group — drag-and-drop between Documentation and API Reference is not supported.

If the reference is ordered first, is published and there are no documentations, then it will be the default reference to load for your readers.