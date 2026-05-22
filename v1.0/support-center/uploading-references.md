---
type: page
title: Importing References
listed: true
slug: uploading-references
description: 
index_title: Importing References
hidden: 
keywords: 
tags: 
---

To upload a new reference or to override an existing reference, you may either do it using our [API](/support-center/api-key) or through the editor as such:

- In the editor top navigation, open the section menu.
- Click **+ New API reference**.
- Choose **Upload OpenAPI definition**.
- Choose a valid OpenAPI 2/3 (Swagger) JSON or YAML file.
- Wait until validation and parsing is complete.

On parsing completion, you will be notified that the reference has been created. If parsing or validation failed, an error will appear.

{% callout type="info" title="Overwrite by Name" %}
If you upload a reference with the same title, then your reference will be overwritten and updated. Your old reference will not be available anymore.
{% /callout %}

## Best Practices for API References

Ensure that every operation has a unique operation ID. Operation IDs are used in %product% for linking to endpoints.

### Validation Fail

We will notify you of detailed validation errors if any do exist. To interactively fix them, open the reference in our [API Editor](/support-center/edit-references) — the issues panel at the bottom lists every error and jumps to the offending line on click.

### Limitations

Maximum upload size allowed is 8MB.