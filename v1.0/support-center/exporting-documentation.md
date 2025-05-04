---
type: page
title: Exporting Documentation
listed: true
slug: exporting-documentation
description: 
index_title: Exporting Documentation
hidden: 
keywords: 
tags: 
---

Your data is exclusively yours. You have the freedom to export it whenever you choose, ensuring you maintain control over your information at all times.

We offer project exports in two convenient formats:

- [Darkdown](/support-center/exporting-documentation#darkdown): Use if you wish to re-import the data into %product% later with no data loss.
- Markdown: Use for external purposes.

## Darkdown

[Darkdown](/support-center/importing-documentation#darkdown-format) is our unique version of Markdown. When a project is exported and subsequently imported back, Darkdown ensures that the following elements are preserved:

[Darkdown](/support-center/importing-documentation#darkdown-format)

- All the published and draft text in each page.
- All the blocks in each page with every configuration and detail.
- The order of the pages.
- Categories and external links.
- Documentation settings.

## Exporting a Project

To export a project:

- Open Project Settings {% icon classes="fas fa-layer-group inv-icon" /%} from the sidebar.
- Click Export {% icon classes="fas fa-upload" /%}.
- Choose the export format. The active project will be exported.

The download process will take just a few seconds, after which you will receive a compressed file in the ZIP format. This file includes all versions of the product, comprehensive documentation, API references, and indices pertaining to the documentation. The structure of the file is organized as follows:

{% image url="https://uploads.developerhub.io/prod/8gDX/8f5nld9kg0bt3ainyzorna5vifgu9wdy9ry210sz479muvfno7bp34zn8gn5vdaf.png" mode="set" height="704" width="464" %}
{% /image %}

To learn how to import this export back into %product%, please refer to the detailed instructions available at [auto$](/support-center/importing-documentation).

## Exporting a Page

To export a page:

- In the documentation index, please select the desired page that you wish to export.
- Click on Export {% icon classes="fas fa-upload" /%} under the title.

The export will be in %product% [Darkdown format](/support-center/importing-documentation#darkdown-format).

## Exporting Images

To export the images from your %product% project, please follow these detailed steps:

- Get a [markdown export](/support-center/exporting-documentation#exporting-a-project) of your project first.
- Unzip the export.
- Use our tool [mdimg](https://github.com/developerhub-io/mdimg) which finds all the URLs in the export and downloads the images. You can find already built binaries for linux and mac in the [releases](https://github.com/developerhub-io/mdimg/releases/tag/v1.0.0).