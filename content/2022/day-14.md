---
title: "2022 Day 14: Sand Everywhere"
date: 2022-12-13T22:37:29-08:00
tags: [ 'advent-of-code', '2022' ]
images: ['/images/2022-day14-v2.gif']
---
Day 14, we're trapped in a cave that's being filled in by sand.

<!--more-->

I really enjoyed this puzzle, actually. It reminded me of those early particle
sandbox simulators.. I found a couple bugs in my AOC library in the process.
Oops.

## Visualization

Figuring out how many full particle paths to show was tricky. If I had a little
bit more mental energy (and time to run the rendering) I'd like to do something
like a particle path heat map, or at least do motion blurring of the particles.
As it is, we see a few paths, and then switch to rendering first 10% of settled
states, and then 2% of settled states.

I threw in a particle counter in the top left because, well, I have font
rendering code and I may as well use it.

### Update `2022-12-14`

I had a bit of inspiration and realized I can visualize this as a continuous
flow of sand, if I'm careful about the order of updating particles. Et voila!

![Day 14 Visualization v2](/images/2022-day14-v2.gif)

### Original

![Day 14 Visualization](/images/2022-day14.gif)

## New Features

No new features, but I'm working on supporting for blending a stack of frames
into a single frame to produce motion blur effects. Stay tuned, hopefully we'll
see something later this year...
