---
type: page
title: Tabs
listed: true
slug: tabs
description: 
index_title: Tabs
hidden: 
keywords: 
tags: blocks
---

Tabs serve as an effective tool for organising instructions tailored to various customer segments, specific objectives, or diverse implementations. By separating content into distinct sections, they enhance user experience and ensure that relevant information is easily accessible.

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
- When switching to a tab, all other tab blocks on the page having the same title will also get switched to automatically.
- When switching to a tab, when visiting another page in the docs, all the tab blocks will switch to the same tab title if possible automatically. 

## Tabs Known Limitations

The following are known limitations of tabs:

- While tab contents are searchable, if a search result exists in the non-default tab, the tab will not be switched to on choosing that search result..
- Tabs cannot contain other tabs.