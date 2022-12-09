---
title: "2022 Day 8: Trees But Not A Tree Problem"
date: 2022-12-08T20:28:38-08:00
tags: [ 'advent-of-code', '2022' ]
images: ['/images/2022-day08.gif']
---
Day 08 has us counting trees, in two ways.

<!--more-->

Part A asks us to count trees visible from the perimeter. There are surely more efficient ways, but scanning rows & columns gets us there easily.

Part B asks us to find the tree from which we can count the most trees in the cardinal directions. (It's a little more complicated than this, because we multiply out the directions and not add, but that's the gist.)

## Visualization

I opted to include both parts in the visualization. I don't think either part stands alone, but gluing them together with the context of a device / software is I think quite lovely.

![Day 08 Visualization](/images/2022-day08.gif)

## New Features

This was the first puzzle this year where the GIF took a while to render. To
help with this, I actually parallelized the canvas rendering phrase, where we
convert our 2D glyph array into pixels.

I also added several new glyphs to help here, `✔`, `-`, and `+` (though `+` did
not end up used in the final rendering.)
