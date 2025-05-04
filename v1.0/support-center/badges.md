---
type: page
title: Badges
listed: true
slug: badges
description: 
index_title: Badges
hidden: 
keywords: 
tags: 
---

Badges serve as informative labels and play an integral role in %product%'s inline blocks.

## How to add a Badge?

To add a badge, start typing "/" and choose **Badge** from the inline block list.

## Badge Examples

{% badge type="primary" text="Primary" /%} {% badge type="success" text="Success" /%} {% badge type="warning" text="Warning" /%} {% badge type="info" text="Info" /%} {% badge type="error" text="Error" /%} {% badge type="custom" text="Custom" /%}

## Advanced Configuration

The custom badge can be easily modified via [Custom CSS](/support-center/custom-css) to adopt any color of your choice. Additionally, you can adjust its color dynamically based on the content it contains:

{% code %}
{% tab language="css" title="Custom CSS" %}
.customise .cbadge.custom[data-text="Pink Badge"] {
  color: white !important;
  background: #ff536b !important;
}

.customise .cbadge.custom[data-text="Purple Badge"] {
  color: white !important;
  background: #6d53ff !important;
}
{% /tab %}
{% /code %}

Would yield {% badge type="custom" text="Pink Badge" /%} and {% badge type="custom" text="Purple Badge" /%}.