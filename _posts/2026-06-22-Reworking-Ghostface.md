---
layout: post
title: Reworking Ghostface
subtitle: Turning it into an ornament
thumbnail-img: /assets/img/reworking_ghostface/thumbnail.jpg
gh-repo: daattali/beautiful-jekyll
tags: [Cosplay]
comments: true
mathjax: true
---

I guess we're not done!

Last time I wanted to retire my **[previous cosplay](https://bnzel.github.io/2025-05-29-Cosplay-V2/)** but my mind kept thinking about the day where things went haywire. I put it off for some time as I was distracted by other projects and honestly tried to convince myself it's not a **BIG** deal. Well my stubbornness got the best of me...

Unfortunately I did not cosplay during **Anime North 2026** because I was taking my **SWEET TIME** making sure I don't repeat the same mistakes with previous cosplays.

### What Was The Problem Again?
The LED matrices started glitching out during my leave from the convention and I suspected it was either loose wires or something was shorting the data lines of the modules that corrupted the signal. It's not surprising since I was subjecting the mask to vibrations and motions due to me walking around. The weather also played a big part.

The mask was also heavy so it always drooped down and I had to readjust which might have contributed to the problem.

I decided that it will look better as a display.

### So How Did You Solve it?
When I toke a look back at the mask, I realized my first mistake was soldering all the matrices together. This made it extremely difficult to troubleshoot and pinpoint if whether the problem was a single or multiple modules. So I tested a new LED matrix on the microcontroller and unfortunately it seems like the pins themselves had issues.

To confirm my suspicion I used a spare Pro Trinket and tested the old matrices on the new microcontroller, and it still won't work. That meant that the old trinket and matrices was damaged.

Starting from scratch it is... Fortunately I had 6 more backup LEDs and daisy chained them with dupont wires to make my life easier. I removed the animation switching, Neopixels and LED strips because I won't be wearing it anymore.

There was also another problem that was in the code, I didn't explicitly defined what LED intensity to start with, this caused all the 6 LEDs to pull alot of current that sometimes glitched the animations. This was the line I added ```setIntensity(1);```.



### What Does It Look Like Now?
![demo](../assets/img/reworking_ghostface/demo.gif)

Yup, not much *(<small>sorry to disappoint</small>)*. The only major difference is adding a hoodie (which I made from torn sweatpants). But hey I hanged it on my wall!

![mask hanged on wall](../assets/img/reworking_ghostface/hanged_on_wall.gif)

### So You're Really Done?
I really think so. I'm pretty satisfied how this turned out as an ornament...