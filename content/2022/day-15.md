---
title: "2022 Day 15: Overlap"
date: 2022-12-14T22:21:28-08:00
tags: [ 'advent-of-code', '2022' ]
images: ['/images/2022-day15.png']
---
Day 15 challenges us to handle very large overlapping areas.

<!--more-->

Part A tempts us into brute-forcing a solution. It's doable, and it works fine.
Part B is not amenable to brute-force, though there is a "trick", which in
retrospect I think is pretty obvious. (It's so obvious in retrospect it's hard
to think of it as a "trick". But it took me 30min of noodling to get there,
so.)

I think there are potentially non-brute-force solutions for Part A that are
effective solutions for part B as well, involving compressing space into
intervals.

## Visualization

There's not a lot of "motion" in this problem, though we could illustrate the
search. Still, it's interesting to see the problem space visually.

![Day 15 Visualization](/images/2022-day15.png)

## New Features

I have a working prototype of stacking ultra-high-framerate renderings to
produce usable GIFs. The motion seems a lot smoother to me (rendering at
1000fps and then blurring together 50 frames), but there's still some work to
do. Stay tuned. Or not. You do you.
