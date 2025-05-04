---
type: page
title: Theme
listed: true
slug: theme
description: 
index_title: Theme
hidden: 
keywords: 
tags: 
---

Docs in %product% can have two themes:

- Light theme {% icon classes="far fa-sun" /%}
- Dark theme {% icon classes="fas fa-moon" /%}

You can set a default theme for readers, allowing them to customize their experience by switching to a preferred theme. Furthermore, a toggle can be displayed, enabling readers to easily change the theme according to their personal preferences.

## Setting the theme

To modify the default theme for readers, follow these steps:

- Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Under Customisation, choose the theme.
- Click Save.

{% callout type="success" title="Code Theme" %}
We recommend utilizing the [light code theme](/support-center/code-theme) in conjunction with the light theme for an optimal viewing experience.
{% /callout %}

## Show Theme Toggle

To show a theme toggle for readers:

- Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Under Customisation, check Show Theme Toggle.
- Click Save.

## Light Theme

{% image url="https://uploads.developerhub.io/prod/8gDX/mrt1abt8rg987708qel6e1h9s0utudtwmvucjekdauu3jorobegsyq9ya61nh508.png" mode="responsive" height="1846" width="3110" %}
{% /image %}

## Dark Theme

{% image url="https://uploads.developerhub.io/prod/8gDX/chbacjezburq4q9ra3l872jr6l1jq5nv78d5eaix2yjx9bh9sinq2549xhkt9695.png" mode="responsive" height="1846" width="3110" %}
{% /image %}

## Modifying the theme

To modify the theme, you can either update the [CSS Variables](/support-center/custom-css#css-variables) as needed or add your own [auto$](/support-center/custom-css). When the dark theme is applied, a global `.dark-mode` CSS selector is added to `document.body`.