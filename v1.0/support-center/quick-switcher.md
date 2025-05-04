---
type: page
title: Quick Switcher
listed: true
slug: quick-switcher
description: 
index_title: Quick Switcher
hidden: 
keywords: 
tags: 
---

As your documentation expands, navigating through an extensive index can become increasingly challenging. The Quick Switcher feature streamlines this process, enabling you to locate content more efficiently and effortlessly.

Quick switcher is able to perform the following:

- **Find Page**: Search for a page or an API reference by title or slug (case insensitive).
- **Find Text**: Search for text in pages only (case insensitive).
- **Find & Replace**: Finds text in pages and replaces it (case sensitive).

{% callout type="info" title="Info" %}
This feature is exclusively accessible within the editor. However, your readers will have the capability to utilize the global search directly.
{% /callout %}

## How to open Quick Switcher

To open the quick switcher, click on the search bar, press `⌘/Ctrl + K`, or select the search icon {% icon classes="fas fa-search inv-icon" /%} located in the bottom right corner. Once the quick switcher is open, type in your search query and press enter to select the best result.

## Search Mode: Find Page

The Find page allows you to search across all pages and API references based on both title and slug for the current version you are using. This feature incorporates typo-tolerance, ensuring that your search results are relevant even if there are minor spelling errors.

{% image url="https://uploads.developerhub.io/prod/8gDX/3vdjs3p4hwvl6uv4q8j8kjh0fpo03bfmmz8y3hg1dtgxes0xmdep6haavgai8yfx.png" mode="responsive" height="1070" width="2150" %}
{% /image %}

## Search Mode: Find Text

The text search functionality allows you to search through all pages in the current version for specific text. The search operates using the format [Darkdown](/support-center/exporting-documentation#darkdown) and is not case sensitive, meaning it will identify matches regardless of whether the text is in uppercase or lowercase.

{% image url="https://uploads.developerhub.io/prod/8gDX/3g9fjg5fxbu8j3zz8v07gnhl31pogeb93ljib3w8xvws6zyqoftfc2cdv9mcbm63.png" mode="responsive" height="1064" width="2074" %}
{% /image %}

## Search Mode: Find & Replace

The Find & Replace feature enables you to search through all pages in the current version for specific text, allowing you to replace the text directly. The search is conducted using the [Darkdown](/support-center/exporting-documentation#darkdown) format and is case sensitive, ensuring that you target the precise text you wish to modify.

Before making any replacements, you will be presented with all occurrences that can be replaced for your review.

{% image url="https://uploads.developerhub.io/prod/8gDX/kgabsm00ade1v8hl1dvpqrbs5yrmnjp4itn1pacvi4h0j85yctl5wq8xhn9nltar.png" mode="responsive" height="1072" width="1758" %}
{% /image %}

{% callout type="warning" title="Warning" %}
Once text has been replaced, the operation cannot be reversed. Please ensure that you thoroughly check all occurrences and confirm that you want ALL of them to be replaced before proceeding.
{% /callout %}

## Notes about Quick Switcher

Find Text and Find & Replace search through [Darkdown](/support-center/exporting-documentation#darkdown) format, with this come a few notes:

- Search performed is exact text search. This means that it is not typo tolerant.
- To search in formatted text like "pied **piper**", you'd need to search for `pied **piper**`. Searching for `pied piper` will not yield results.
- Text in [blocks](/support-center/blocks) is also searched. Text in [auto$](/support-center/custom-html) and [auto$](/support-center/synced-blocks) among other dynamic blocks is not searched.
- Text in links is not searched.
- Text in [inline blocks](/support-center/blocks#inline-blocks) is not searched.