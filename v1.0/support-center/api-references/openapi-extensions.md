---
type: page
title: OpenAPI Extensions
listed: true
slug: openapi-extensions
description: 
index_title: OpenAPI Extensions
hidden: 
keywords: 
tags: 
---

The following extensions are available on %product%:

## x-tagGroups

`x-tagGroups` serves to group operations within the index, effectively establishing an additional hierarchy. This feature is activated exclusively when the [index is configured to be collapsible](/support-center/api-reference-settings#allow-index-to-collapse).

In OpenAPI, tag groups can be defined in the following manner:

{% code %}
{% tab language="yaml" %}
openapi: '3.0'
info: ...
tags:
  - name: Lion
  - name: Cheetah
  - name: Dolphin
  - name: Octopus
x-tagGroups:
  - name: Feline
    tags:
      - Lion
      - Cheetah
  - name: Sea
    tags:
      - Dolphin
      - Octopus
{% /tab %}
{% /code %}

## x-enum-varnames

`x-enum-varnames` gives a secondary name for an enum.

Enum var names can be defined as such in OpenAPI:

{% code %}
{% tab language="yaml" title="" %}
Animal:
  type: integer
  enum:
    - 33
    - 21
  x-enum-varnames:
    - Dog
    - Cat
{% /tab %}
{% /code %}

## Variables

In addition to utilizing [variables](/support-center/variables) throughout the API references, you can also leverage these variables in the following ways:

- `%_.project.base_path%` for project base path.
- `%_.version.slug%` for version slug.
- `%_.section.slug%` for API reference slug.

These variables are particularly valuable for creating links within markdown descriptions.