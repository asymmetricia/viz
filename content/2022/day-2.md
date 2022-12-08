---
title: "2022 Day 2: Slot Machine?"
date: 2022-12-01
tags: [ 'advent-of-code', '2022' ]
---
Day 2 was a rock-paper-scissors simulator, in an interestingly backwards sense. 

<!--more-->

You're given a list of the other player's play, and an instruction to win,
lose, or draw. Each outcome has a score value, earning different points based
on the symbol you throw, and what the outcome is.


## Visualization

I chose to visualize counters for each of the nine outcomes, and tally the
score as we progress.

![Day 2 Visualization](/images/2022-day02.gif)

## New Features

This visualization highlights **two** new features:

1. Text boxes; the line drawing characters were already present, but this
   functionality makes it easy to draw a self-sizing box with content, header,
   and footer at an arbitrary location on the page.

2. Block Text, which is pretty meta and fun: Instead of rendering the font with
   individual pixels, block text renders the same font using `#` symbols, which
   are themselves them rendered via the font.
