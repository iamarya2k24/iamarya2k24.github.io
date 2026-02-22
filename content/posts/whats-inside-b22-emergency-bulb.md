---
title: "Surya B22 Inverter Bulb Teardown: Fix Blinking Issues & Battery Failure"
date: 2026-02-22T16:30:03+05:30
weight: 2
aliases: ["/inside-a-b22-emergency-bulb"]
tags: ["diy", "electronics"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "A deep dive into the Surya B22 rechargeable bulb: Featuring a 2600mAh Enerzone 18650 battery and 34 LEDs. Learn how to disassemble and diagnose circuit failures."
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
    image: "/images/IMG_2727-EDIT.jpg" # image path/url
    alt: "my avatar" # alt text
    caption: "my avatar" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/iamarya2k24/iamarya2k24.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

# Introduction

I purchased the __Surya B22 Emergency LED__ bulb back in 2021 to handle frequent power outages. Since I didn't have a home UPS or inverter at the time, this "plug-and-play" rechargeable bulb was a perfect, affordable solution for keeping the lights on.

However, after a few years of service, the bulb started malfunctioning. Instead of steady light, it began **blinking incessantly**. Curious about the failure, I decided to take it apart to find the root cause.


## How to Disassemble a Surya Rechargeable LED Bulb

1. Remove the Diffuser: The plastic dome at the top can usually be pried off with a flat-head tool.
2. Expose the LED Plate: Inside, you’ll find the aluminum PCB housing 34 high-brightness LEDs.
3. Access the Base: I pried the bottom plug (B22 connector) to release the internal assembly.


## Why is my Surya Emergency Bulb Blinking?
Blinking in rechargeable LED bulbs usually indicates a failure in the power delivery cycle, either the LED driver circuit is failing, or the Lithium-ion battery can no longer hold a stable charge or take a charge.


![LED Top view without the diffuser](/images/IMG_2729-EDIT.jpg#center)

You can see that the bulb has 34 LEDs inside.


I moved the bottom half of the bulb and managed to twist it out, exposing the circuit board inside and a removable battery.

![18650 Li-ion battery](/images/IMG_2728-EDIT.jpg#center)


The Li-ion battery is made by Enerzone India. Rated at 3.7volts x 2600 mAh. 

![LED Driver Circuit](/images/IMG_2727-EDIT.jpg#center)

## Inside the Surya Emergency Bulb: Components & Discovery
Upon twisting out the internal assembly, I found a surprisingly modular setup. The heart of the bulb consists of a control circuit and a removable battery.

1. The Battery (The Likely Culprit)
The unit uses a standard 18650 Li-ion battery made by Enerzone India.
Specs: 3.7V | 2600 mAh.

> Observation: I noticed black soot near the battery protection circuit. It appears a capacitor or a component on the protection board has >blown. While the battery cells might have some residual voltage, the protection board's failure means it can no longer accept a charge or discharge safely.

2. The LED Driver Circuit
The circuit is relatively simple. One side handles the AC-to-DC conversion and charging, while the other side contains the logic chips to switch between "Mains" mode and "Battery" mode during a power cut.

> Technical Note: The failure mode here is the internal safety board of the battery. When these protection circuits fail (often with a "boom" or soot mark), the driver circuit gets confused, leading to the "strobe" or blinking effect you see.


## Conclusion: Is it Fixable?
My teardown suggests that the LED chips themselves are fine; the issue lies entirely with the 18650 battery pack. Because the battery is removable and uses a standard 3.7V rating, this is seems to be repair friendly.

**My Next Step**: I will try replacing the 18650 battery with a fresh one and check if the blinking stops. I’ll report back with the results!

## Stay Updated
If you found this teardown helpful, you can follow this blog via [RSS](https://iamarya2k24.github.io/index.xml) or find me on [Mastodon](https://fosstodon.org/@null0x0) for more DIY repair guides and tech experiments.
