---
type: page
title: Inline Images
listed: true
slug: inline-images
description: 
index_title: Inline Images
hidden: 
keywords: 
tags: 
---

Inline images are images that can be seamlessly integrated within tables, callouts, or any other content areas. They enhance the visual appeal and help convey information more effectively.

## How to add an Inline Image?

To add an inline image, start typing "/" and choose **Image** from the inline block list.

Additionally, when you paste an image within a table, it will be inserted as an inline image seamlessly within the table cell.

## Inline Image Modes

Inline images support two modes which you can modify by clicking on the image and selecting one. The modes are:

- Fit width: The image will stretch to fill the entire width of the container. If the image's natural width is smaller than the container, it will display at its natural width. This mode is the default for images pasted into a table.
- Resizable: The image can be resized, but it cannot be made larger than its natural size.

## Inline Image Examples

{% table widths="173,0" %}
| Type of Animal | Sound | How it looks like | 
| ---- | ---- | ---- | 
| Cat | Meow | {% inline-image url="https:\\/\\/uploads.developerhub.io\\/prod\\/02\\/kgnzg0ig37q5lyjn3sxwjekoxmvcio2qf4s1sutk77z61157kyih40xtxrj7p05l.png" width="113" /%} | 
| Dog | Woof | {% inline-image url="https:\\/\\/uploads.developerhub.io\\/prod\\/02\\/o4y7fb9jve2gbw4zdq1j3p5b5txg9aio7vymkjrnle44j8fcsizrccj3nd0oo9o3.png" width="88" /%} | 
{% /table %}