---
title: "2022 Day 18: Hot Stuff"
date: 2022-12-18T12:35:55-08:00
tags: [ 'advent-of-code', '2022' ]
images: ['/images/2022-day18.png']
videos: ['/images/2022-day18.mp4']
---
On Day 18, we have lava rain.

<!--more-->

The lava falls into a pool of water, and we estimate how long it'll take to
cool by calculating the surface area of the lava droplets. The droplets are
composed of voxel cubes, and we only count surface area that water can reach-
the laval droplets have internal air bubbles.

My solution desginates a square outside of the boundary of the droplet as
"outside", and then incrementally designates reachable empty squares as
outside, within a box around the droplet.

Once this is done, we identify surfaces that touch the outside just by checking
whether the neighbor is "outside" or "nothing".

## Visualization

The visualization shows the two phases of the problem- propagating squares
defined as outside, and then scanning the droplet to identify outside-touching
cubes.

This was a pretty easy solve for me, which is nice, because it gave me a bunch
of extra mental energy to do some cool visualization work!

{{< video src="/images/2022-day18.mp4" >}}

## New Features

Wow! So much.

### Bug Fixes

First of all, I had a bug in the line-drawing code in
[github.com/asymmetricia/pencil](https://github.com/asymmetricia/pencil), which
was not properly computing alpha as part of the process of aliasing. Fixed!

### `isovox`

Next is `isovox`. My first pass at rendering this used `fauxgl`. `fauxgl` is
lovely, but when it comes to me and AoC visualizations, it feels a little
cheaty.

So, I wrote my own isometric voxel rendering, which can render three dimension
isometric grids of colored cubes at arbitrary resolution, with alpha.

### GIF Alpha Blending Palettes

The next challenge was taking these now rather complicated images and producing
GIFs from them. I spent a lot of time playing with palettes and Floyd-Steinberg
dithering. Ultimately I settled on augmenting the Tol vibrant palette with the
colors from the WebSafe palette to use when blending/dithering. This produced
pretty good results!

But it also produced 150MiB GIFs.

### Direct MP4 Rendering

In the past, when my visualizations produced large GIFs, I'd just suck it up,
keep them, and transcode them to MP4 for sharing. This produces somewhat
sub-optimal results. Especially in this case, where the pipeline becomes:

1. Go renders bitmap in memory
2. Go palletizes bitmap to a GIF
3. Go difference-optimizes the GIF
4. Go renders the GIF to disk
5. ffmpeg / handbrake renders the GIF to mp4 (manually)

Wow!

But it turns out you can just feed ffmpeg a stream of PNG files, and with the
right options it will happily render them directly to a video file.

So, with the help of some goroutines, I now have a procedure to fire up ffmpeg,
and render images then hand them off to ffmpeg to encode into video. And that's
what you see here!

See you next time, folks.
