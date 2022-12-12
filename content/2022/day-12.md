---
title: "2022 Day 12: A STARry-eyed Surprise"
date: 2022-12-11T23:21:36-08:00
tags: [ 'advent-of-code', '2022' ]
images: ['/images/2022-day12.gif']
---
On the twelfth day of advent, we do some hill-climbing.

<!--more-->

Ironically, we don't use a hill-climbing algorithm for this. Part A challenges
us very directly to do some path-finding. Part B asks us to instead find the
best starting point.

I used a pre-prepared implementation of `A*` for Part A, and it was more than
fast enough to brute-force Part B. (With a small additional to my `World`
implementation to make it easier to get a list of positions corresponding to a
given `rune`.)

It was only while I was working on the visualization that I realized I could
simply reverse the direction of path-finding, flip the "neighbor" rules around,
and path-find down from the end. This required tweaking `A*` to accept a set of
goals instead of a single goal, but that was easily done. A really good
heuristic for this would be difficult to write, but those are just a
performance improvement..

## Visualization

The interesting thing about `A*` is that the visualization of the traversal
varies greatly based on the heuristic, even for the same outcome.

I have yet to see an Advent of Code challenge where the heuristic is truly
important (it's primarily a performance optimization); perhaps in one of those
"infinite space" type of problems?

So usually, I only tune the heuristic for an interesting visual.

![Day 12 Visualization](/images/2022-day12.gif)

## New Features

Aside from the improvement to `A*` mentioned above, I also improved the way the
`Canvas` GIF renderer supports variable framerates. Previously, the renderer
was provided a range of frames and the framerate to apply there. Now, each
frame has its own timing. This should make precisely-timed animations (e.g.,
multi-phase or accelerating) much easier to work on.
