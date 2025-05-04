---
type: page
title: FAQ
listed: true
slug: api-reference-faq
description: 
index_title: FAQ
hidden: 
keywords: 
tags: 
---

## Why is the request/response body empty even with a schema object present?

Ensure that your [schema object](https://swagger.io/specification/#schema-object) includes a defined type. If a type is not specified, the table will display the text `<type>`. Merely having `properties` present does not suffice to indicate that the schema is categorized as an object.

For example:

{% code %}
{% tab language="yaml" title="Bad ❌" %}
content:
	application/json:
    schema:
      properties:
        id:
          type: number
        name:
         type: string
{% /tab %}
{% tab language="yaml" title="Good ✅" %}
content:
	application/json:
    schema:
      type: object <-- added
      properties:
        id:
          type: number
        name:
         type: string
{% /tab %}
{% /code %}

### How do I reorder Operations?

Operations, such as `GET /version` and `POST /reference`, are organized in the precise sequence they appear within the OpenAPI definition. Although we employ `tags` to categorize these operations for easier navigation, it's crucial to understand that we maintain their original order without any modifications. For instance:

{% code %}
{% tab language="yaml" %}
# If the operations and tags are specified as such in the API definition:

paths:
	'/cat':
  	post:
    	tags:
      	- Cats
      ...
    get: 
    	tags:
      	- Cats
      ...
  '/dog':
  	get: 
    	tags:
      	- Dogs
      ...
    post: 
    	tags:
      	- Dogs
      ...
tags:
	- name: 'Dogs'
  - name: 'Cats'
  
# The operations and tags would be ordered as such in the API reference:

# Dogs
#   GET  /dog
#   POST /dog
# Cats
#   POST /cat
#   GET  /cat
{% /tab %}
{% /code %}

You are encouraged to rearrange the operations within your OpenAPI definition to create an optimal and seamless experience for your readers. This flexibility allows you to present the information in a way that enhances understanding and navigation through your API documentation.

{% callout type="warning" title="Cannot use API editor to reorder" %}
Unfortunately, due to limitations in the API editor, reordering operations from the source view has no effect. To achieve the desired reordering, you must make the changes locally in a file and then upload the modified file as an API reference import for the changes to take effect.
{% /callout %}