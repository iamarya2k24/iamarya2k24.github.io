---
title: "Post #4"
date: 2026-06-30T16:30:03+05:30
weight: 1
aliases: ["/my-oracle-cloud-experience"]
tags: ["oracle"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "My experience with Oracle cloud free tier."
canonicalURL: "https://iamarya2k24.github.io/posts/content"
disableHLJS: true # to disable highlightjs
disableShare: true
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "/images/arya-profile-photo.jpg" # image path/url
    alt: "my avatar" # alt text
    caption: "my avatar" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/iamarya2k24/iamarya2k24.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

# Getting started with Oracle cloud.

I have been curious about Oracle cloud for a while and I got to try their free tier last weekend and here are my thoughts.

Initial thoughts
---

## Frustration:

I want to note that with _Oracle cloud free tier_ launching the __Ampere__ arm type/class of instance is almost impossible as it currently falls under capacity limits.

>You need to upgrade to pay as you go plan. I reached out to oracle chat support and am able to confirm this. For paid account you will be charged refundable deposit of $100. 

>> I have requested them that this needs to be highlighted at the time of sign-up and as well as the official documentation as it is currently a waste of time to create a free tier account without signing up for paid tiers. Seems almost like ^a^ ^scam^ ^to^ ^me^ IMO.

>>> I would personally _prefer_ if they restricted new signups for _free tier_.

>>>>I would also like to note that Oracle is [heavily debt ridden][1] right now with its **AI** bet. I wouldnt use the free tier for anything serious. They have already reduced the limits from 4xOCPU_24.GB to 2xOCPU_12.GB RAM.


Overview:
---

This is a high level diagram depicting a typical dev env on OC.

> **Note:** If you want IPv6 address for your instances, you need to create a custom VCN and enable IPv6 support, create subnets, routes with IPv6 addresses.

![](/images/Clipboard_2026-06-30-02-29-05.png)

### Current state of the project: **HOLD**
---

I will update the post with more details as I try and configure my instance with the software I use.

[https://web.archive.org/web/20260627234609/https://www.cnbc.com/2026/06/26/oracle-stock-ends-worst-week-since-2001-as-investors-dwell-on-finances.html][1]

[1]: cnbc.com


