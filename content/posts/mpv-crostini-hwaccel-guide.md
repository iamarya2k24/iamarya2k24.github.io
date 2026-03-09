---
title: "mpv on ChromeOS with Hardware acceleration"
date: 2026-03-08T16:30:03+05:30
weight: 1
#aliases: ["/first-post"]
tags: ["linux", "mpv", "chromeos", "guides", "linuxOptimization", "h264"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Run customized mpv on ChromeOS with hardware acceleration"
canonicalURL: "https://iamarya2k24.github.io/posts/content"
disableHLJS: true # to disable highlightjs
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "/images/mpv-screenshot-1.png" # image path/url
    alt: "screenshot of mpv player on linux/crostini/chromeos" # alt text
    caption: "a screenshot of mpv player on debian crostini" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/iamarya2k24/iamarya2k24.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

# Custom mpv with hw accel with vaapi + vogpu + crostini on chromeOS

## Introduction

**Y**ou can watch videos on ChromeOS with the inbuilt player. But if you are like me and use Debian (crostini), then having a dedicated media player to watch the content makes more sense. 

*mpv* is an [amazing media player](https://mpv.io/manual/stable/) with so many customization options. I have used it previously on *Micro**SLOP** Windows 10* and was wondering if I can set up mpv with hardware acceleration on chromeOS. 

Without the hardware acceleration the *playback* is *super stuttery* and audio/video is desynced. In this post, I discuss how to set up the config for mpv to enable smoother playback.

## Prerequisites

1. Chromebook with crostini support, You can enable it by launching Chrome browser, navigate to `chrome://flags/#crostini-gpu-support`, enable the flag and restart the system.
2. Check if the hw is detected using `glxinfo -B` and `see “Device: virgl”`
3. Download `mpv, xclip, ffmpeg` and other dependencies
4. Clone the mpv-config [GitHub repo](https://github.com/iamarya2k24/mpv-config).

> Note: *ASUS C423NA* doesn't support av1 encode/decode on my device.

## Steps

1. Copy the content of the repo to the mpv config folder. On Linux it is stored in `~/.config/mpv/mpv.conf`
2. Edit the file, add the following to it.
```bash
~/.config/mpv/mpv.conf
# Enable GPU accel, Read the [official mpv manual](https://mpv.io/manual/stable/#gpu-renderer-options)
vo=gpu
hwdec=vaapi

# NOTE: disable or alter the config parameters as per the hardware.

```

3. Open a video file with mpv and enjoy the smooth playback.

## Screenshots

![A screenshot of mpv running on ChromeOS](/images/mpv-screenshot-1.png#center)

![A screenshot of mpv running on ChromeOS](/images/mpv-screenshot-2.png#center)


**Sources:**
- [Reddit](https://old.reddit.com/r/cloudygamer/comments/qz08xx/chromebook_enabling_hardware_acceleration_for/)
- [mpv manual](https://mpv.io/manual) 
- [Arch Linux Wiki](https://wiki.archlinux.org/title/Chrome_OS_devices/Crostini)
- [YouTube video](https://www.youtube.com/watch?v=xoJu8UBExd4) used in the screenshots.





 