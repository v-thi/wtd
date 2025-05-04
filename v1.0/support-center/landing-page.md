---
type: page
title: Landing Pages
listed: true
slug: landing-page
description: 
index_title: Landing Pages
hidden: 
keywords: 
tags: 
---

Help your readers easily locate the resources they need directly from Hello!

There are two types of Landing Pages:

- Main landing page: The page that lives at the root `/` of the docs site.
- Other landing pages: These are pages that reside on different paths within the site structure. Additionally, certain other landing pages can be designated specifically as 404 error pages, serving as user-friendly notices when requested content cannot be found.

{% image url="https://uploads.developerhub.io/prod/8gDX/dbvfs91re3vdnrn94lyaq9fx1lbuq54g4j3yknkgx3kxtn6n5jl85oq9n3lc159e.png" mode="responsive" height="709" width="1035" %}
{% /image %}

## Main Landing Page

The main landing page is a modern entry point for your readers to understand your developer hub. It shows your project’s content compactly on one page. The content is organized in card format, with each card linking to a documentation or category, based on the [structure](/support-center/landing-page#cards-generation-strategy) of your project.

## Main Landing Page Contents

Main landing page contains two main sections:

- **Hero**: A customizable title accompanied by a button that directs users to the default page of your developer hub.
- **Cards**: An automatically generated collection of cards that provide direct links to specific sections of your developer hub. These cards enhance navigation and improve accessibility, allowing users to quickly find relevant information within the hub.

## Cards Generation Strategy

Cards are automatically generated based on the structure of your developer hub. The card generation strategy operates as follows:

### Documentation

- If your developer hub has multiple documentations, each documentation is shown in a card. Categories and pages for each documentation are listed in the card.
- If your developer hub has one documentation, each category appears in a card that lists the pages within it. If there are no categories, a single card lists the pages.

## References

Every reference is contained in its own card.

## Customizing Landing Page

You can customize the main landing page like this:

- **Hero background**: In your sidebar under Landing Page, you can select a pattern for the background. The color matches your [main colour](/support-center/customising-visuals#changing-colours).
- **Hero title**: You can change the title directly from your Landing Page by editing it.
- **Hero button**: You can change the button text by clicking on it. You can also remove the button entirely.

All landing pages can be enabled or disabled as needed from the sidebar as well.

The META description for the landing page can be easily modified through its settings.

You can further customize by using the [Custom CSS](/support-center/custom-css) and [Custom Javascript](/support-center/custom-javascript) features.

## Custom Landing Page

If you want to use a custom landing page or write your own HTML/CSS/JS, read [auto$](/support-center/custom-landing-page).

## Adding Landing Pages

To create a new landing page, at a path other than `/`, follow these steps:

1. From the sidebar, choose {% icon classes="fas fa-rocket inv-icon" /%} Landing Pages.
2. Click on {% icon classes="fas fa-plus" /%} Create new landing page.
3. Type in the path for the page to exist on (without basepath if any).
4. Click Save.
5. Customise it by clicking on Edit HTML.

## Removing Landing Pages

To remove a landing page, other than the main landing page, follow these steps:

1. From the sidebar, choose {% icon classes="fas fa-rocket inv-icon" /%} Landing Pages.
2. Choose the landing page you wish to delete.
3. Click on Delete at the top right.

## 404 Page

A landing page can be set as a 404 page. When someone visits an unrecognized URL, they will be taken to this 404 page. To set a landing page as a 404 page:

1. From the sidebar, choose {% icon classes="fas fa-rocket inv-icon" /%} Landing Pages.
2. Choose the landing page you wish to designate.
3. Click on the settings {% icon classes="fas fa-cog" /%}
4. Toggle Use as a 404 Page.

{% callout type="warning" title="One 404 page" %}
Only one 404 page can exist in the project
{% /callout %}