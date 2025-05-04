---
type: page
title: Tabs
listed: true
slug: tabs
description: 
index_title: Tabs
hidden: 
keywords: 
tags: 
---

Tabs serve as an effective tool for organizing instructions tailored to various customer segments, specific objectives, or diverse implementations. By categorizing content into distinct sections, they significantly enhance the user experience and ensure that relevant information is easily accessible. This structured approach not only improves navigation but also allows users to quickly find what they need, ultimately streamlining their interaction with the material.

To create tabs:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Tabs {% icon classes="fas fa-folder" /%}

## Tab Example

{% tabs %}
{% tab title="Android" %}
To set up the SDK, do the following:

1. Get the SDK from the website.
2. Run gradle.
3. Add an import as such to the code:

{% code %}
{% tab language="java" %}
import AwesomeSDK;
{% /tab %}
{% /code %}

## Example Android Code

{% code %}
{% tab language="java" %}
package com.example.helloworld;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
   @Override
   protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);
      setContentView(R.layout.activity_main);
   }
}
{% /tab %}
{% /code %}
{% /tab %}
{% tab title="iOS" %}
To set up the SDK, do the following:

1. Get the SDK from the website.
2. Run cocopods.
3. Add an import as such to the code:

{% code %}
{% tab language="swift" %}
import AwesomeSDK
{% /tab %}
{% /code %}
{% /tab %}
{% /tabs %}

## Tab Block Features

The following are features of the tab block:

- It can have as many tabs as visually possible.
- Every tab has its own title, and is linkable.
- Headings inside tabs can be used with [page linking](/support-center/page-linking).
- Tab contents are searchable.
- Tab contents can contain all kinds of blocks and formatting supported by %product%
- When you switch to a tab, all other tabs with the same title on the page will switch automatically as well.
- When you switch to a tab or visit another page in the docs, all tab blocks will automatically switch to the same tab title if possible.

## Tabs Known Limitations

The following are known limitations of tabs:

- You can search through tab contents, but clicking on a search result from a non-default tab won't switch to that tab.
- Tabs cannot contain other tabs.