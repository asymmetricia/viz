---
title: "2022 Day 7: A Directory Tree 🎄"
date: 2022-12-06
draft: false
---
Day 7 involved parsing the output of a shell transcript. 

<!--more-->

There are narrower solutions to solve just the puzzle, but like many people I
opted to parse the transcript into an in-memory tree.

## Visualization

The visualization for today shows parsing progress and current state, by
rendering the "stack" of directories up to the "current" directory, and
populating its contents as we read the input file.

![Day 7 Visualization](/images/2022-day07.gif)

## New Features

The main memorable enhancement here is the addition of a `/` glyph.
