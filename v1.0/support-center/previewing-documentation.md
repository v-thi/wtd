---
type: page
title: Previewing Documentation
listed: true
slug: previewing-documentation
description: 
index_title: Previewing Documentation
hidden: 
keywords: 
tags: 
---

%product% was designed to unify the view between the editor and the live version.

There is no need to preview your documentation. The editor already is showing you the same view of how it will look to your documentation readers 😉

{% callout type="success" title="Woah!" %}
What was I thinking before?!
{% /callout %}

If you are really keen on previewing it, then you can see it live by publishing it.

## URL Strategy

The URL, which is the link you see in your browser, plays a crucial role in determining which project, version, and section (documentation or API reference) are currently being accessed. It specifies the exact resources the user wishes to view, allowing for a seamless navigation experience across different parts of the documentation.

Here is a summary of how we load resources using URLs:

{% table widths="388" %}
| URL | Result | 
| ---- | ---- | 
| `https://<project>/<section>` | Loads the default page in the specified documentation, or the specified API reference in the default version. | 
| `https://<project>/<documentation>/<page>` | Loads the page in the specified documentation in the default version | 
| `https://<project>/<version>/<section>` | Loads the default page in the specified documentation, or the specified API reference in the specified version | 
| `https://<project>/<version>/<documentation>/<page>` | Loads the specified page in the specified documentation in the specified version | 
| `https://<project>/` | Loads the landing page if enabled, or the default page in the default section of the default version | 
{% /table %}

The following URLs have been deprecated and are no longer recommended for use. However, for backward compatibility, they have been redirected:

{% table %}
| URL | Redirected To | 
| ---- | ---- | 
| `https://<project>/<version>/-/-` | `https://<project>/<version>/<documentation>` | 
| `https://<project>/<version>/<documentation>/-` | `https://<project>/<version>/<documentation>` | 
| `https://<project>/<reference>/ref` | `https://<project>/<reference>` | 
| `https://<project>/<version>/<reference>/ref` | `https://<project>/<version>/<reference>` | 
| `https://<project>/-/-/-` | `https://<project>/<section>` | 
{% /table %}

Any other form of link will load the default page.

You can add a base path if you are [hosting under your own existing website](/support-center/hosting#hosting-under-your-own-custom-domain). The same rules apply, but the base path will be added right after the `<project>`. For example, instead of `https://<project>/<version>/<documentation>/<page>`, the link would be `https://<project>/<base-path>/<version>/<documentation>/<page>`.

## Print-Optimized

Our pages are print-optimized (specially for A4 paper size). We recommend having the wide documentation layout when printing, and always printing from the published documentation site (not on the editor). If you are an enterprise customer, then you may also [export an entire version as PDF](/support-center/pdf-export).

{% image url="https://uploads.developerhub.io/prod/8gDX/3lmhzjyqdyxlpxseucjwoqcesxxee9u0u2843iodjlbf7dm5shwebyl6svraln6v.jpg" mode="responsive" height="2270" width="2832" %}
{% /image %}

## Embed Mode

%product% sites can be embedded using `iframe` as needed. This is specially helpful if you wish to create a documentation widget so your reader can follow the instructions without leaving their tabs.

There are two types of embed mode:

- Minimal: Hides the top navigation, footer, index and table of contents. Mode is `embed`.
- Normal: Hides the top navigation and footer only. Mode is `embed_full`.

{% callout type="info" title="Note" %}
In scenarios where the window width is small, minimal and normal modes exhibit similar behavior. This is because both the index and the table of contents are hidden by default when the window width is reduced.
{% /callout %}

Embed mode can be turned on by adding a `?mode=embed` or `?mode=embed_full` to any %product% URL (except landing pages). For instance, to show users the page at `[https://dev.company.io/ios/getting-started](https://dev.company.io/ios/getting-started)`, you can load an `iframe` with `src="[https://dev.company.io/ios/getting-started?mode=embed"](https://dev.company.io/ios/getting-started?mode=embed&quot;)`.

{% code %}
{% tab language="markup" title="HTML" %}
<iframe style="position:fixed;width: 500px;height: 450px;background: white;right: 100px;bottom: 0px;z-index: 10;border: 1px solid #bbb;border-radius: 5px;" src="https://docs.developerhub.io/support-center/uploading-references?mode=embed"></iframe>
{% /tab %}
{% /code %}

Here is a preview:

{% image url="https://uploads.developerhub.io/prod/8gDX/1woh5xa6urcb2hchq5a5mo5dg4dstqkepelmdm1758d6jyxqrr5azl1hlapda7n5.png" mode="responsive" height="1755" width="3112" %}
{% /image %}