---
title: "Day 6 - Message Markers"
date: 2022-12-05
---
In day 6, we're looking for start of message markers in a series of bytes.

<!--more-->

An optimization I _didn't_ implement here is that we can skip scanning subsets
when we find a byte pair, because the next legal subset must be at least after
the first member of the pair.

## Visualization

The viz here is straightforward- we visually indicate our scanning range, with
some UI embellishments.

![Day 6 Visualization](/images/2022-day06.gif)

## New Features

I don't remember what (if anything) I added here!
