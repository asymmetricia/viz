---
title: "2021 Day 8: One Dimensional Sudoku"
date: 2021-12-07
tags: [ 'advent-of-code', 'YYYY' ]
images: ['/images/YYYY-dayDD.gif']
---
On Day 8, we reverse a mapping of on/off signals to the 7-segment digits they
represent.

<!--more-->

This puzzle was fun, but challenging. We're given a series of "words", each of
which corresponds to a 7seg digit. It's essentially a problem of figuring out a
logic mapping. Given, for example, `af`, we know that the digit must be `1`
(the only digit with two lighted segments). We don't know which segment is `a`
or which is `f`, though. There are four such unique-count digits, and we can
use this data to determine a mapping of segments.

This would've been a great way to use the 7seg implementation I built for 2022
Day 6, but alas, 12/5/2022 comes after 12/7/2021 according to most calendars.

## Visualization

The visualization walks through each "display" in the mapping and visualizes
the collapse down into known digit values.

![Day 8 Visualization](/images/2021-day08.gif)

## New Features

No new features per se, but for today we created the glyph for the pipe `|`
characters. The split pipe harkens back to a common feature of monospace fonts
from my youth.
