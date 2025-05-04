---
type: page
title: Importing Documentation
listed: true
slug: importing-documentation
description: 
index_title: Importing Documentation
hidden: 
keywords: 
tags: 
---

%product% provides powerful tools to enable you to easily move your content around, edit it and restructure it, all out of the editor.

## Import Sources

You can import data to %product% from a variety of sources:

- %product% export (available for entire project imports and one page imports)
- [Markdown](/support-center/external-sources#markdown-import)
- [ReadMe](/support-center/external-sources#readme-import)
- [Zendesk](/support-center/import-from-zendesk)
- Other sources, such as: [HTML](/support-center/external-sources#importing-from-html), [Confluence](/support-center/external-sources#importing-from-confluence), [Word](/support-center/external-sources#importing-from-word-documents) or [other external sources](/support-center/external-sources).

## Import DeveloperHub.io Export

To import documentation, follow these steps:

- Make sure your import files are [structured](/support-center/importing-documentation#structuring-files) as required.
- From the sidebar, open Project settings {% icon classes="fas fa-layer-group inv-icon" /%}
- Click on Import {% icon classes="fas fa-download" /%}
- Choose %product%.

Importing could take a few seconds up to a minute.

{% callout type="info" title="Info" %}
All imports are designed to add version information. It’s important to note that versions, documentation, and pages are never overwritten, ensuring the integrity and historical accuracy of your data.
{% /callout %}

## Import a page into %product%

You can import a single Markdown file or a [Darkdown](/support-center/importing-documentation#darkdown-format) page at a time into %product%. This streamlined process allows for easy integration and ensures that your content is formatted correctly for optimal use within the platform.

To import one page, follow these steps:

- From the index, choose the page to import over, or create a new page and save it.
- Under the title, click on Import icon {% icon classes="fas fa-cloud-download-alt" /%}
- Choose the file to be imported.

## Structuring Files

To import documentation from %product% export into %product%, it is essential to organize your files according to the following structure:

{% image url="https://uploads.developerhub.io/prod/8gDX/gdjrdpzqetrabvbmo4vrkrvq6w346ul1ya2he3pe1dsfdkobbnmn8x9yy5bitog7.png" mode="responsive" height="704" width="722" %}
{% /image %}

Where, for example:

- `v1.0` is the name of your version.
- `Support Center` is the title of your documentation.
- `1 Getting Started.md` is a documentation page written in Darkdown format. Its order is 1st in Support Center documentation and its title is `Getting Started`. `Getting Started` folder indicates that `1 Getting Started.md` is a parent page, and it has a subpage titled `First Steps`.
- `1 Formatting Text.md`, `2 Keyboard Shortcuts.md` and `3 Using Markdown.md` are all subpages of Writing Documentation page.
- `settings.json` is `Support Center` documentation settings file. Settings file is an optional file.

Every parent page must include a Markdown file along with a corresponding folder that shares the exact same name.

The orders must be incremented, beginning from 1. If an order is not provided in the filename, there is no assurance that the index order will be maintained.

Additionally, you can enhance your project by including OpenAPI specification files within a designated folder named `refs`, located in the corresponding version folder. This allows for better organization and accessibility of your API documentation.

All files included in the import process must be compressed into a ZIP file format.

## Darkdown Format

Darkdown Format is simple. Each file must contain a header and optionally content.

### Header

Each file contains a header depending on the index element being described.

- Page:

{% code %}
{% tab language="yaml" %}
---
type: page
title: Callouts
listed: true
slug: callouts
description: <SEO description>
index_title: Callouts
hidden: 
keywords: keyword1,keyword2
tags: tag1,tag2
---
{% /tab %}
{% /code %}

- Category:

{% code %}
{% tab language="yaml" %}
---
type: category
title: Start Here
---
{% /tab %}
{% /code %}

- Link:

{% code %}
{% tab language="yaml" %}
---
type: link
title: Go to DeveloperHub.io
url: https://developerhub.io
---
{% /tab %}
{% /code %}

- Separator:

{% code %}
{% tab language="none" %}
---
type: separator
---
{% /tab %}
{% /code %}

### Content

Category, link, and separator elements do not contain any content. In contrast, pages are rich with content, which can consist of pure Markdown or a combination of Markdown along with our advanced blocks annotation features.

The contents of draft and published pages can be clearly defined in an export, distinguished by the use of a `<code>---draft</code>` or `<code>---published</code>` header. For example:

{% code %}
{% tab language="yaml" %}
---draft

Draft content is here

---published

Published content is here
{% /tab %}
{% /code %}

An example of published content that includes a heading, descriptive text, and a code block is as follows:

{% code %}
{% tab language="yaml" %}
---published
## Code Block Example

A Hello World code block:

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "console.log(\"Hello World\");",
                "language": "javascript"
            },
            {
                "code": "print(\"Hello World!\")",
                "language": "python"
            },
            {
                "code": "package main\n\nimport \"fmt\" \n\nfunc main() {\n     fmt.Println(\"hello world\")\n}",
                "language": "go"
            }
        ]
    }
}]$
{% /tab %}
{% /code %}

### Blocks

Since Markdown lacks support for many of our powerful features, we developed Darkdown formatting to incorporate these advanced capabilities. All blocks are exported in the following manner:

{% code %}
{% tab language="yaml" %}
$plugin[{
     "type": "<<type>>",
     "data": "<<data>>"
}]$
{% /tab %}
{% /code %}

Where the type is one of the following: `code-block`, `image`, `video`, `table`, `github-code`, `synced-block`, `tab-block`, `index-list`, or `custom-html`. The data definition varies depending on the specific type selected.

### Inline Blocks

Additionally, inline blocks are exported in Darkdown format, such as [badges](/support-center/badges), [icons](/support-center/icons), and [keyboard keys](/support-center/keyboard-keys). For example,

This badge: {% badge type="success" text="Great!" /%} would be formatted as:

{% code %}
{% tab language="yaml" %}
{% badge type="success" text="Great!" /%}
{% /tab %}
{% /code %}

And this icon: {% icon classes="fas fa-adjust" /%} would be formatted as:

{% code %}
{% tab language="yaml" %}
{% icon classes="fas fa-adjust" /%}
{% /tab %}
{% /code %}

You are welcome to export any page to gain insights into the formatting of its content. This allows you to better understand the layout and structure used throughout the application.

## Table Format

Tables are exported in Markdown format by default. However, if the column width is specified, we will utilize the Darkdown format to ensure that all information is preserved accurately.

The Markdown format for tables utilized in imports and exports is structured as follows:

{% code %}
{% tab language="none" %}
| Browser | Mode | Is Supported? | Remarks | 
| ---- | ---- | ---- | ---- | 
| Chrome | Desktop | Yes | Fully supported | 
| Chrome | Mobile | Yes | Fully supported |
{% /tab %}
{% /code %}

Requirements:

1. All rows start and end with `|`.
2. Every column is separated by `|`.
3. A header row must exist.
4. A separator row under header must exist.
5. Multiline cells use `\n` to separate lines.

## Image Import

When an image is referenced using Markdown format on any of the pages, it will be automatically downloaded to our servers. Subsequently, it will be served from our content delivery network, ensuring efficient and reliable access for users.

Images can be uploaded from two distinct sources:

- HTTP, or
- Local

Regardless of the image source, it is essential that each image does not exceed a maximum file size of 10MB. Exceeding this limit will result in the import process failing.

{% callout type="warning" title="Warning" %}
By importing images on %product%, you are responsible for ensuring that you have the necessary rights to all data. It is important to verify that you possess the appropriate licenses or permissions for any images used to avoid potential copyright infringements.
{% /callout %}

### HTTP Image Import

To import images from the internet, please ensure they are referenced using the following format:

{% code %}
{% tab language="markdown" %}
HTTP Image:

![Image Caption](https://example.com/image.png)
{% /tab %}
{% /code %}

The image will subsequently be downloaded from its source and uploaded to our content delivery network. It's essential that the image is publicly accessible online; otherwise, the import process will fail.

### Local Image Import

To successfully import images locally from the provided ZIP file, ensure that they are located in a folder named `assets`, which should be placed alongside the versions. This organizational structure is essential for proper access and retrieval of the images during the import process.

They should be referenced as such:

{% code %}
{% tab language="markdown" %}
Local Image:

![Image Caption](/assets/image.png)
{% /tab %}
{% /code %}

Inside `assets` folder, any folder structure is allowed.