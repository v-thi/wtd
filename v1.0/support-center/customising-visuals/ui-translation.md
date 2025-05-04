---
type: page
title: UI Translation
listed: true
slug: ui-translation
description: 
index_title: UI Translation
hidden: 
keywords: 
tags: 
---

If you would like to customize the %product% UI text displayed to your readers, which is set to English by default, you have two options for modification:

- Changing the Language from Documentation {% icon classes="fas fa-book inv-icon" /%} settings.
- Modifying the [javascript](/support-center/custom-javascript).

## Which Text Can be Changed?

{% image url="https://uploads.developerhub.io/prod/8gDX/ckijtlxtqsrppnueicnqo469wmsd08k7h8cge0rj9drbigktlaulq2m66ve8siyu.jpg" mode="responsive" height="724" width="1185" %}
{% /image %}

All text displayed on the user interface (UI) that we provide can be translated for your audience. This encompasses text found on the landing page, within the search functionality, in the table of contents, as well as the version and section selectors.

The text that is available to be translated is detailed as such:

{% code %}
{% tab language="javascript" %}
{
  navbar: {
    home: 'Home',
  },
  tableOfContents: {
    title: 'On This Page'
  },
  search: {
    title: 'Search',
    singularResult: 'Showing ? search result',
    results: 'Showing ? search results',
    all: 'All',
    startTyping: 'Start typing to search...',
    searchTags: 'Search Tags',
    ai: {
      title: 'Search or ask a question',
      pressEnterToAsk: 'Press enter to ask',
      aiEnabled: 'AI enabled',
      askingAi: 'Asking AI',
      disclaimer: 'AI answers may be incorrect, incomplete or misleading. Refer to the sources.',
      answer: 'Answer'
    }
  },
  landingPage: {
    showAll: 'Show All',
    view: 'View',
  },
  documentations: 'Documentation',
  references: 'References',
  versions: 'Versions',
  page: {
    nextToRead: 'Next to read',
    relatedPages: 'Related pages',
    update: {
      lastUpdated: 'Last updated',
      by: 'by',
      on: 'on'
    },
    feedback: {
      prompt: 'Was this page helpful?',
      placeholder: 'Do you want to tell us more?',
      send: 'Send',
      skip: 'Skip',
      thankYou: 'Thank You!',
      yes: 'Yes',
      no: 'No'
    }
  },
  warnings: {
    oldVersion: 'You are viewing an older version. Click here to view the latest'
  },
  consent: {
    accept: 'Accept',
    text: 'We serve cookies on this site to analyse traffic and optimise your experience. By using the website you agree to the +Privacy Policy+.'
  },
  '404': {
    largeText: '404',
    smallText: 'It seems you are lost',
    button: 'Go back'
  }
}
{% /tab %}
{% /code %}

## Translate UI Text

To specify the language in which the UI text should be displayed, please follow the steps below:

- From the sidebar, choose Documentation {% icon classes="fas fa-book inv-icon" /%}
- Next to the title, click on Settings {% icon classes="fas fa-cog" /%}
- Next to Language, select the language to translate the UI text to.

Each documentation can have its own translation.

At the moment, we have support for English, French, Deutsch and Spanish. If there is a language which you need for your documentation which we do not provide yet, then please [contact us](/support-center/contact-us).

## How to Customize UI Text

{% html %}
<div class="grow-border text-left">
<div class="grow-star">⭐</div>
    Available in Grow Projects
</div>
{% /html %}

By using [custom javascript](/support-center/custom-javascript), you can modify any or all of the default translations. For example, you can add a script to your HEAD tags to override table of contents and search results as such:

{% code %}
{% tab language="html" title="Javascript" %}
<script>
  window.translations.apply({
  	tableOfContents: {
      title: "Tabla de contenido"
    },
    search: {
      results: "Mostrando ? resultados de búsqueda",
      singularResult: "Mostrando 1 resultado de búsqueda"
    }
  });
</script>
{% /tab %}
{% /code %}

{% callout type="info" title="Info" %}
Some translations may include variables, such as `search.results`, which will be substituted with the actual number of search results. It is essential to retain the question mark in the translation, as it marks the position for where the number will be inserted.

Other translations such as `consent.text` have plus signs where a URL should be added.
{% /callout %}

### Change Translation According to Content

To change the UI text based on the selected version or documentation, you can use [custom javascript](/support-center/custom-javascript). Here is an example code you can use:

{% code %}
{% tab language="html" title="Javascript" %}
<script>
	document.addEventListener('onsectionchange', function (event) {
        if (event.detail.type === 'documentation') {
            if (event.detail.slug === 'EN') {
				window.translations.tableOfContents.title = 'On This Page';
            } else if (event.detail.slug === 'DE') {
				window.translations.tableOfContents.title = 'Inhaltsverzeichnis';
            }
        }
    });
</script>
{% /tab %}
{% /code %}