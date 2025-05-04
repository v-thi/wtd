---
type: page
title: API Reference Settings
listed: true
slug: api-reference-settings
description: 
index_title: API Reference Settings
hidden: 
keywords: 
tags: 
---

Along with [code generation](/support-center/code-generation), each API Reference includes a set of configurable settings that you can manage. To access these settings, simply click on the Settings {% icon classes="fas fa-cog" /%} icon located in the sidebar under the Reference section.

{% image url="https://uploads.developerhub.io/prod/8gDX/bkbinuxlks6w58b38o4kbmnk6g8rynjs4rcex7ku3uz9mhgqzo8cuthtvskty9ba.png" mode="responsive" height="529" width="446" %}
{% /image %}

## Allow Download

The "Allow Download" setting enables users to download the API Reference conveniently by displaying a button at the top of the page. This feature enhances accessibility, allowing users to easily obtain and reference the documentation offline.

## Show Try It Out

Enables [auto$](/support-center/try-it-out), allowing you to seamlessly test APIs directly from the API Reference.

## Show Content-Type Header

For operations that require a request body in OAS3 (OpenAPI Specification 3.0), enabling this option will automatically display a header in the example that specifies the content type. For instance:

{% code %}
{% tab language="bash" %}
curl --request POST \
 --url https://api.developerhub.io/api/v1/version/{versionId}/reference \
 --header "Content-Type: application/json" # <--- This line would be added 
 --form "file=@{file}"
{% /tab %}
{% /code %}

## Show Accept Header

For operations exclusive to OAS3, enabling this option will display a header in the example that specifies the accepted response media type. For instance:

{% code %}
{% tab language="bash" %}
curl --request GET \
 --url https://api.developerhub.io/api/v1/page?version_id={version_id}&version_slug={version_slug}&documentation_id={documentation_id}&documentation_slug={documentation_slug}&page_slug={page_slug}&format={format} \
 --header "Accept: application/json"
{% /tab %}
{% /code %}

## Allow Tags to be Expand

If your API Reference contains a large number of items, loading them all at once may result in slower performance. To enhance efficiency, you can enable the option to allow tags to expand. By activating this feature, you can seamlessly load an API Reference of any size without experiencing any performance degradation. This optimization allows for a smoother and more responsive user experience.

When tags are permitted to expand, the corresponding tag will be displayed along with its description. Additionally, a comprehensive table listing all operations available under this tag will be presented. A button labeled "Show" will also appear, allowing users to reveal the operations conveniently.

{% image url="https://uploads.developerhub.io/prod/8gDX/zwfbvc7gtjse82gpsr35rgfcke0grn66jpj7k9znp2b46d2rzhe5fc3ijvsbrukl.png" mode="responsive" height="489" width="1410" %}
{% /image %}

## Allow Index to Collapse

When this option is enabled, the tags in the index become collapsible, allowing for a more organized and streamlined view.

## Auto-Capitalize Tags

When this option is enabled (default setting), tags will automatically be capitalized, ensuring that the first letter of each word is in uppercase.

## Show Request Example Code Samples

When checked by default, it enables the option for users to select a code library and view a corresponding code sample. However, when unchecked, the interface will only display an example URL or request body, limiting the ability to explore code samples in various libraries.