---
title: "2024 Day 16: Complicated Mazes"
date: 2024-12-17T18:55:37-08:00
tags: [ 'advent-of-code', '2024' ]
images: ['/images/2024-day16.gif']
---
Day 16 is ostensibly a "simple" maze solution, but with a twist- going in a
straight line from tile to tile is cheaper than turning.

<!--more-->

This has been the most enjoyable puzzle of 2024 so far. Familiar enough-
bouncing between Dijkstra's Algorithm and A\*; but very thought provoking.

The solution I ended up using was to perform A\* twice, once from the start
point and once from the endpoint, and then count all squares where the sum of
the cost from the start to that square and the cost from that square to the end
is equal.

## Visualization

The visualization shows the pass of performing A\* in each direction, and then
a simple scan highlighting the "best path" tiles.

{{< video src="/images/2024-day16.mp4" >}}

## New Features

The major new feature here is tweaking the `TolScale` function to produce
colors along sequential palettes. I added the `Incandescent` palette, and also
actually built interpolation between values.

... 

Interpolation is mostly not useful because most of my image functions work with
paletted images, but perhaps that's something worth changing; at least as long
as I'm producing `h.264` and `PNG`. GIFs will forever be paletted.
