---
type: page
title: Custom Footer
listed: true
slug: custom-footer
description: 
index_title: Custom Footer
hidden: 
keywords: 
tags: 
---

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

Apply a custom footer to match your website.

Unlike [auto$](/support-center/documentation-footer), this footer is situated outside of the documentation container and is created using HTML. Consequently, the custom footer functions as a standalone webpage, complete with its own unique styles and scripts.

## How to set a custom footer

To customize the footer:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the Sidebar.
- Under Customize, select Edit Footer {% icon classes="fas fa-code" /%}
- Enter the custom HTML, and select Done.
- Refresh the page to see the changes.

The footer can also be set to use full width from the same settings window.

The custom HTML is encapsulated within an iFrame, which is required to include both a head and a body section. To optimize performance, we recommend linking your website's styles and scripts directly in the head instead of writing them in the footer. This practice allows for better caching of the footer content, enhancing load times for returning users.

{% callout type="warning" title="Links" %}
If you have any links in the footer, make sure that you use `target="_parent"` to navigate inside the parent, not the iframe itself.
{% /callout %}

{% callout type="warning" title="Use Only HTTPS" %}
Load assets only from HTTPS sources, otherwise your readers will see a "Not Secure" badge next to the browser URL.
{% /callout %}