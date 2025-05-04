---
type: page
title: Code Theme
listed: true
slug: code-theme
description: 
index_title: Code Theme
hidden: 
keywords: 
tags: 
---

%product% supports both light and dark themes for code blocks. We recommend using the light code theme for your whole project when using the [light theme](/support-center/theme).

## Setting Light/Dark Code Theme

To switch the code theme between light and dark modes, follow these steps:

- Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
- Under Customisation, choose the Code Theme.
- Click Save.

## Advanced Code Theming

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

We utilize CodeMirror for the rendering and formatting of our [code blocks](/support-center/code-blocks). CodeMirror offers a wide variety of themes for your selection. You can explore the complete list of available themes [here](https://codemirror.net/demo/theme.html#default).

To change the code theme, you need to import the theme stylesheet and provide a [setting](/support-center/advanced-settings) that specifies the theme to use. This ensures your selected theme is applied correctly in the application.

- First, find a CDN providing the stylesheet of the theme for maximum performance. [cdnjs](https://cdnjs.com/libraries/codemirror) is an example.
- Import the theme stylesheet by add such a style tag using [auto$](/support-center/custom-javascript):

{% code %}
{% tab language="css" %}
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.60.0/theme/ambiance.min.css">
{% /tab %}
{% /code %}

- Apply the theme settings also by adding a script to your HEAD tags:

{% code %}
{% tab language="html" %}
<script>
    window.settings.apply({
      code: {
        darkTheme: 'ambiance',
        lightTheme: 'xq-light'
      }
    });  
</script>
{% /tab %}
{% /code %}

{% callout type="info" title="Note" %}
Changes will only show in live mode
{% /callout %}

{% callout type="success" title="Own themes" %}
You can also create your own themes and use them in the same way
{% /callout %}

You might want to change the styling of the code block tabs and the copy button to match the theme you have chosen.