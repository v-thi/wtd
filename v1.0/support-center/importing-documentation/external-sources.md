---
type: page
title: External Sources
listed: true
slug: external-sources
description: 
index_title: External Sources
hidden: 
keywords: 
tags: 
---

%product% allows documentation to be imported from external sources. The documentation must be supplied in markdown format.

## How to Import Documentation?

To import documentation, follow these steps:

- Make sure your import files are structured as required.
- From the sidebar, open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%}
- Click on Import {% icon classes="fas fa-download" /%}
- Choose the appropriate import source.

Importing could take a few seconds up to a minute.

You could also import a single page, see [Import a page into DeveloperHub](/support-center/importing-documentation#import-a-page-into-product) for instructions.

{% callout type="info" title="Info" %}
All imports add versions. Versions, documentations and pages are never overwritten.
{% /callout %}

{% callout type="warning" title="Limits" %}
The maximum upload size is 5MB. Contact us if your documentation has a larger size.
{% /callout %}

## Structuring Files

To import documentation from any external sources into %product%, it is essential to format your files according to the specified structure:

{% image url="https://uploads.developerhub.io/prod/8gDX/kfbply33iq1ibigabbv7itmaa3qh32923u9j046hwvcxs6pepcmq6y0r8uwc3us7.png" mode="responsive" height="636" width="694" %}
{% /image %}

Where:

- `v1.0` is the name of your version.
- `Support Center` is the title of your documentation.
- `Getting Started.md` is the title of a documentation page written in Markdown format. `Getting Started` folder indicates that `Getting Started.md` is a parent page, and it has a subpage titled `First Steps.md`.
- `Formatting Text.md`, `Keyboard Shortcuts.md` and `Using Markdown.md` are all subpages of Writing Documentation page.

Every parent page must have a corresponding Markdown file and a folder that bear the exact same name.

Additionally, you can include OpenAPI specification files in a directory named `refs` within the version folder.

## Limitations of External Sources Import

The integration of external sources is regrettably constrained by the insufficient information present in the imports. The limitations include:

- Ordering of the pages.
- Other index elements, such as categories and external links.

## Markdown Import

To successfully import from Markdown, it's essential to adhere to the specified file structure outlined above. The first line of any page should be designated as a Heading 1, formatted as `# Title`. This line will automatically be converted into the page title.

### What is supported?

1. Code blocks
2. Tables
3. Images
4. Callouts (without title - Title defaults to Info)

## ReadMe Import

To successfully import from ReadMe, it is essential to adhere to the specified file structure outlined above. Please note that all internal links will be automatically adjusted to correspond with the links within your %product% documentation.

### What is supported?

1. Multi-language code blocks
2. Tables
3. Images
4. Videos
5. Callouts
6. Embed
7. Custom HTML

### ReadMe Import Process

To import from ReadMe:

- Get an export file from ReadMe.
- Unzip the file.
- If you have any recipes or changelogs folders (or any folder that is not user-guides related) then delete them.
- Compress the version folders, and use our import tool, choosing ReadMe as import type.
- Your imported versions will be at the bottom of the version list.
- ReadMe does not include order information in their exports, which means you will need to manually reorder the pages to achieve the desired arrangement.
- Once you are ready to publish, publish the versions!

## Importing from HTML

To import HTML, you need to convert it to Markdown first. There are numerous free online services available to assist you with this conversion, such as [h2m](http://tinyambition.com/h2m/) and [turndown](https://domchristie.github.io/turndown/). Additionally, many libraries are available if you prefer to batch convert multiple files simultaneously. Once your documentation is in Markdown format, please refer to the [how to import documentation](/support-center/external-sources#how-to-import-documentation) guide for further instructions.

## Importing from Word Documents

To import documents in Word doc/docx format, you must first convert them to Markdown. A convenient option is to utilize the free online [Word to Markdown Converter](https://word2md.com/). After converting your documents to Markdown format, please refer to the [how to import documentation](/support-center/external-sources#how-to-import-documentation) guide for the next steps.

## Importing from Confluence

To successfully import content from Confluence, it is essential to first convert it into Markdown format. Depending on your Confluence hosting method, there are various approaches available for exporting content to Markdown. These methods may include utilizing Confluence Plugins or leveraging open-source libraries specifically designed for this purpose.

## Importing from Zendesk

See [auto$](/support-center/import-from-zendesk).