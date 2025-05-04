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

To upload a new reference or to override an existing reference, you can do so using our [API](/support-center/api-key) or by utilizing the editor in the following way:

- Open References {% icon classes="fas fa-vector-square inv-icon" /%} from the sidebar.
- Select Import OpenAPI 2/3 Reference {% icon classes="fas fa-plus" /%}
- Choose a valid OpenAPI 2/3 (Swagger) JSON or YAML file.
- Wait until validation and parsing is complete.

Upon the completion of the parsing process, you will receive a notification confirming that the reference has been successfully created. In the event that parsing or validation encounters an issue, an error message will be displayed to inform you of the failure.

{% callout type="info" title="Overwrite by Name" %}
If you upload a reference with the same title, then your reference will be overwritten and updated. Your old reference will not be available anymore.
{% /callout %}

## Best Practices for API References

Ensure that every operation is assigned a unique operation ID. Operation IDs play a crucial role in %product% by facilitating seamless linking to endpoints.

### Validation Fail

We will inform you of any detailed validation errors that may exist. To interactively resolve these validation errors, you can utilize our [API Editor](/support-center/edit-references).

### Limitations

The maximum upload size permitted is 8MB.