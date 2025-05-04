---
type: page
title: Index List
listed: true
slug: index-list
description: 
index_title: Index List
hidden: 
keywords: 
tags: 
---

The index list offers a convenient method for displaying all pages associated with a parent page, allowing for easy navigation and organization of content.

To create an index list:

{% synced id="open-block-menu" %}
{% /synced %}

- Choose Index List {% icon classes="fas fa-list" /%}

A dynamically updating bulleted list will populate with all child pages, each titled and linked for easy navigation. This list automatically adjusts to reflect changes as child pages are added or removed, ensuring that users always have access to the most current content.

{% callout type="info" title="Info" %}
If the page does not contain any child pages, it will appear empty to the readers, as if the block is non-existent.
{% /callout %}

## Example Index List

This is a comprehensive and current list of the child pages associated with this page:

{% index-list %}
{% /index-list %}

It may seem like there is no noticeable difference at first glance. However, that is precisely the intention! The content is generated automatically, ensuring consistency and efficiency in the output.