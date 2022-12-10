---
title: "2022 Day 10: Sprites and Pixels"
date: 2022-12-09T21:30:01-08:00
tags: [ 'advent-of-code', '2022' ]
images: ['/images/2022-day10.gif']
---
Day 10 feels a little meta. We're visualizing pixels on a CRT.

<!--more-->

Initially we're simulating instructions and computing something like a checksum
of the CPU state. Once we pass that, we re-interpret our register as a "sprite"
on a one dimensional line, and mark a pixel as on or off using the cycle
counter as the "clock".

Tracking pixels to draw pixels on the screen.. Reminds me of something.

This is the first problem in 2022 where we're writing a virtual machine. I
really enjoy these puzzles, and while I hope we'll expand on this (remember
Intcode?) this doesn't _feel_ like a starting point for that.

## Visualization

This visualization doesn't require much imagination, but I enjoy the exercise of producing something with some amount of verisimillitude for a "real" system, anyway.

![Day 10 Visualization](/images/2022-day10.gif)

## New Features

No new features today, just a new glyph for ⓒ.
