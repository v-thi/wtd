---
type: page
title: Videos
listed: true
slug: videos
description: 
index_title: Videos
hidden: 
keywords: 
tags: 
---

With our versatile video block, you have the ability to effortlessly embed and upload videos from a wide range of platforms directly into your documentation pages. This feature enhances your content by allowing for richer multimedia integration, making it easier for users to engage with your material.

## Supported Video Platforms

Videos can be embedded natively from:

- Youtube
- Vimeo
- Loom

In addition to the options available, you can provide a URL link to a video file (Raw) or choose to upload one directly. This gives you flexibility in how you manage your video assets.

## How to add Videos?

Follow these steps to add a video to your pages:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Video {% icon classes="fas fa-video" /%}
- Next, choose the provider from the list.
- Paste in the box the URL of the video, or if you chose to upload, select the file.

{% image url="https://uploads.developerhub.io/prod/8gDX/26rodsit4o1xj68h695jk3d74muxxkiavrfcp1rq3weebpea9t5u90wad3wxa2je.png" mode="responsive" height="246" width="1680" %}
{% /image %}

- The video will load instantly and be ready for playback.

{% callout type="info" title="Max video file size" %}
Video uploads are supported with a maximum file size of 10MB.
{% /callout %}

## Example Videos

### YouTube

No music video can compare to the classic appeal of the old Bohemian Rhapsody music video. Additionally, the feature to start the video at a specific time is supported.

{% video %}
{% /video %}

Gotta love that song! 🙌

### Vimeo

Vimeo's interactive video below:

{% video videoId="717779857" provider="vimeo" %}
{% /video %}

### Loom

Loom's own embed video:

{% video videoId="e5b8c04bca094dd8a5507925ab887002" provider="loom" %}
{% /video %}

### URL

Embed videos from your own sources with direct links to the video files:

{% video videoId="http://media.w3.org/2010/05/sintel/trailer.mp4?poster=http://media.w3.org/2010/05/sintel/poster.png&preload=none" provider="raw" %}
{% /video %}

You can enhance your URL by adding search parameters to customize its options. Below is a list of attributes that you can utilize:

:

{% table widths="113,118" %}
| Attribute | Value Type | Description | 
| ---- | ---- | ---- | 
| controls | Boolean | Specifies whether the video should have playback controls. Default is true. | 
| autoplay | Boolean | Indicates that the video will start playing automatically. | 
| loop | Boolean | Indicates that the video will start over again, when finished. | 
| muted | Boolean | Specifies that the video should be muted by default. | 
| playsinline | Boolean | Indicates if the video is to be played inline. | 
| preload | String | Hints to the browser about whether to preload the video (auto, metadata, none). | 
| poster | URL | The URL of an image to show while the video is downloading or until the user hits the play button. | 
{% /table %}

For example: `https://example.com/video.mp4?autoplay=true&loop=true&muted=true&playsinline=true&controls=false` to play the video inline.

## Other Video Platforms

To use other video platforms, you can use [auto$](/support-center/custom-html) block to embed the video.