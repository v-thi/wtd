---
type: page
title: Managing Versions
listed: true
slug: managing-versions
description: 
index_title: Managing Versions
hidden: 
keywords: 
tags: 
---

With %product%, you have the ability to version your documentation effectively. The default version is designated as v1.0, but you can tailor the naming of your versions to suit your needs. While semantic versioning is not mandatory, you are free to incorporate terms like "beta," "alpha," and "latest" alongside traditional version numbers. This flexibility allows you to create a versioning system that best reflects the progress and state of your documentation.

Versioning is very powerful. When pages are [linked](/support-center/page-linking) inside a version, and that version is cloned, all the page links are updated accordingly to the match the new version.

## Creating Versions (Cloning)

New versions are always cloned from other versions. To clone a version:

1. Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
2. Select the version to clone from.
3. Click on "Clone from current version".

{% callout type="success" title="What has happened?" %}
Nice, you cloned a version. That means that every documentation and page under that version has been copied  to the new version.
{% /callout %}

## Publishing Versions

Versions by default are not published. Once you are ready to publish (or unpublish):

1. Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
2. Below the version title at the top, click on the publishing state and modify it as needed.

When a version is published, only the published documentation and API references can be seen by readers. If a version is unpublished, it and all its contents will not be visible to readers, but the publish state of its documentation and API reference remains unchanged.

When a version is published, it will appear with a green dot {% icon classes="fas fa-circle green-text" /%} next to it in the sidebar. When the version is unpublished, it will appear with a red dot {% icon classes="fas fa-circle red-text" /%} next to it.

## Deleting Versions

To delete a version:

- Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
- Select the version to delete.
- Click on the red bin {% icon classes="far fa-trash-alt red-bg-icon" /%} next to the Version title at the top.
- Confirm your deletion.

{% callout type="warning" title="Warning" %}
Once a version is deleted, it cannot be retrieved back.
{% /callout %}

## Ordering Versions

To change a version order in the picker:

- Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
- Drag the version to be ordered from the handle {% icon classes="fas fa-grip-vertical" /%}
- Drop the version in the desired place.

If the version is ordered first and has been published, it will automatically become the default version that loads for your readers. A default badge will be displayed to indicate that this version is set as the default.

The default version does not display its slug in the live page links. For instance, if version 1.0 is set as the default for this documentation project, the live page links will appear without including the version number in the URL.

Accessing `[https://docs.developerhub.io/support-center/managing-versions](https://docs.developerhub.io/support-center/managing-versions)` will automatically redirect you to the default version of the documentation, which is version 1.0. Similarly, using `[https://docs.developerhub.io/v1.0/support-center/managing-versions](https://docs.developerhub.io/v1.0/support-center/managing-versions)` will produce the same outcome.

## Moving Readers to New Version

If your readers have bookmarked pages from older versions, or if they are unaware that your documentation is versioned, it's beneficial to notify them with a banner at the top of the page indicating that there is a newer version available. You can achieve this by using [an advanced setting](/support-center/advanced-settings) and configuring `warnings.oldVersion` to `true`.

{% image url="https://uploads.developerhub.io/prod/8gDX/mr2h9yydbhvyyylfzs3lrw2ehmuj3wjr0ynejz9l08nbwdt5p3mugtelygujxw0e.png" caption="Banner suggesting to the reader that there's a newer version" mode="responsive" height="656" width="1249" %}
{% /image %}

## Locking Versions

Versions can be locked to prevent any further edits to their documentation and API references once they are finalized. When a version is locked, the documentation and API references cannot be modified or updated, ensuring the integrity and consistency of the information presented.

- Created.
- Edited.
- Removed.
- Published.

This also applies to changes made using the [auto$](/v1.0/api/ref).

To lock/unlock a version:

- Click on Version {% icon classes="fas fa-code-branch inv-icon" /%} in the sidebar.
- Select the version to be locked/unlocked.
- Open the version settings {% icon classes="fas fa-cog" /%}.
- Check or uncheck the setting Locked.

A lock icon will appear next to the locked version, and the buttons for saving drafts or publishing will be replaced by a button labeled "Locked."