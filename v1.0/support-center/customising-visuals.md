---
type: page
title: Customising Visuals
listed: true
slug: customising-visuals
description: 
index_title: Customising Visuals
hidden: 
keywords: white-labelled, white-label, whitelabel, whitelabelling
tags: 
---


%product% supports the following customisations: [UI](/support-center/customising-visuals#changing-ui) , [CSS](/support-center/custom-css), [Footer](/support-center/custom-footer), [theme (dark mode)](/support-center/theme), logos, header colour, link colour, font and navigation links.


{% image url="https://uploads.developerhub.io/prod/8gDX/3ru3ka47s5fnrkin2ev136qrl50bfo49ikw2v5khv6neag2o6l3dzrk5o65nywcw.png" caption="" mode="set" height="376.734375" width="276" %}
{% /image %}


## Custom CSS and Footer

Check [Custom CSS](/support-center/custom-css), and [auto$](/support-center/custom-footer) pages.

## Changing Logo

To change the logo:

1. Hover over the top navigation and click on Edit Navigation {% icon classes="fas fa-edit" /%} in the top left corner.
2. Click "Change" next to Logo.
3. Choose the new logo.

You can also change [the URL](/support-center/customising-visuals#adding-links--home-button) which is navigated to when the logo is clicked on.


{% callout type="info" title="Logo" %}
It is best to have a wide logo with transparent background
{% /callout %}


To change the website icon (favicon):

1. Hover over the top navigation and click on Edit Navigation {% icon classes="fas fa-edit" /%} in the top left corner.
2. Click "Change" next to Favicon.
3. Choose the new favicon.


{% callout type="info" title="Favicon" %}
We automatically rescale your favicon if it was too big. Note that the favicon only shows on live mode, and not in the editing mode
{% /callout %}



{% callout type="warning" title="Automatic Saving" %}
Logo and favicon will be automatically saved on change without prompt
{% /callout %}


## Changing UI

%product% provides two UIs, %product% Original and %product% Next.

### Original UI

Original UI is the first UI of %product%, notable for its hovering search bar. The different sections and version are hidden behind dropdown, and the index has coloured categories.


{% image url="https://uploads.developerhub.io/prod/8gDX/n82e0irsmxbg8n3o0i8x9yux0rzkqt3v8oto65i88er4u8r3rb8h0wt7p16q414k.png" caption="" mode="responsive" height="1434" width="2454" %}
{% /image %}


### Next UI

Next UI is the new UI. Next UI features a sleek design where different sections are visible in the top navigation, and a redesigned index with clearer margins and animation. It also providers a better [search experience](/support-center/using-search#next-ui-search).


{% image url="https://uploads.developerhub.io/prod/8gDX/3cu1puv9ewoe3z0fw2src24qizyqcaskehzozhf6rk66hf2m1zdohh9ouygct2bm.png" caption="" mode="responsive" height="1432" width="2456" %}
{% /image %}


To change the UI:

1. Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Customisation, choose which UI to use.
3. Click Save.


{% callout type="info" title="Navigation bar sections" %}
In Next UI, the different sections are laid out in the top navigation bar. In mobile layout, they would collapse into a section picker dropdown.
{% /callout %}


## Changing Colours

The header, link and navigation colours are modifiable. To change the colours:

1. Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Customisation, choose which colour to change.
3. Pick the desired colour (We will warn you if the colour is not contrasting enough)
4. Click Save.


{% image url="https://uploads.developerhub.io/prod/8gDX/1q8gw1310zsp3qp9gpy8qzvzjalskv9eaji0oerm4bouis59m8vj5v18d6p0x9pk.png" caption="" mode="set" height="547.703125" width="372" %}
{% /image %}



{% callout type="info" title="Link Colour" %}
Make sure to set the link colour distinct from the font colour. This is usually your secondary brand colour. The text in your pages is almost black in light theme (white in dark theme), so you need a colourful link for it to be distinguished.
{% /callout %}


## Changing Font

To change the font of the entire project:

1. Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Customisation, edit the font.
3. Choose from the list of Google Fonts available. The font will be previewed immediately in the current documentation.


{% image url="https://uploads.developerhub.io/prod/8gDX/0euo50usnokm8mdlovqanefzbs6agubkkhaix02j57hyrngxq0jnha1o9uj08k2w.png" caption="" mode="responsive" height="718" width="1320" %}
{% /image %}



{% callout type="warning" title="Automatic Saving" %}
Font will be automatically saved on change without prompt
{% /callout %}



{% callout type="info" title="Paid Plan" %}
Changing font is only a paid plan feature
{% /callout %}


### Not using Google Fonts?

If you are not using Google Fonts, you can serve your own font to your documentation portal as described in our own blog post: [Using your own Custom Font](https://developerhub.io/blog/using-your-own-font/)

### Font Weights Missing?

If the font you are using does not have all the font weights we expect, then you can change the actual font weight for an expected one. See [Font Weights](/support-center/custom-css#font-weights).

## Adding Links / Home Button

The logo, and four top navigation links can be setup for external linking to another website, or internal linking inside the documentation. To setup the navigations links:

1. Hover over the top navigation and click on Edit Navigation {% icon classes="fas fa-edit" /%} in the top left corner.
2. Type in the title.
3. Type in the link.
4. Click outside the window to close the top navigation editor and save.

You can change if links open in a new tab or the same tab by checking **Open Links in New Tab**.

The last two links only show in documentations that have wide layout.


{% callout type="info" title="Go Home" %}
Setting the link to `/` goes to the landing page, or the default page if no landing page is setup.
{% /callout %}



{% callout type="warning" title="Automatic Saving" %}
Navigation links will be automatically saved on change without prompt
{% /callout %}


## Sticky Top Navigation Bar

To set the top navigation bar to stick to the top when page is scrolled:

1. Click on Project settings {% icon classes="fas fa-layer-group inv-icon" /%} in the sidebar.
2. Under Customisation, check "Is Top Navigation Bar Sticky?"
3. The setting will be saved immediately.

### Inline Code Colour

Check `--inline-code` in [CSS Variables](/support-center/custom-css#css-variables).

## Need More Customisation?

Check also our [popular customisations](/support-center/css-customisations).

[Let us know](/support-center/contact-us) what you need, we'd love to help!

