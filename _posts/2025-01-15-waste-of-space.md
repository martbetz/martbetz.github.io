---
title: Waste of Space
layout: post
categories: photography computing
---

So here I am, over a decade later, pouting over wasted disk space and thinking “What?! JPEG <i>and</i> raw?! <i>Why the hell am I doing that?!</i>” At least I’ve found the solution: stop it — <i>right now!</i> — and bin those pesky JPEGs! 😶

When I first got hold of my X-T10, I went with ‘[FINE + RAW](https://fujifilm-dsc.com/en/manual/x-t10/menu_shooting/image_quality/index.html)’ (I&nbsp;didn’t know a raw file from a soggy bag of nuts, so it seemed like the safest bet). All those squatting JPEGs, though, have hogged a lot of turf! 

[According to cameramemoryspeed.com](https://www.cameramemoryspeed.com/fuji-x-t10/fastest-sd-cards/), an average X-T10 file-size should sort of look something like this:

- 32.2 MB for raw (RAF)
- 9.1 MB for JPEG (JPG)

Doing a bit of head-math, that’s somewhere around 22% of hogged space — about 220 GB on a 1 TB drive,  almost 7 SD cards at 32 GB each... roughly 6,832 raw files! 😲

<i>Crikey Nora Batty, Bob — we need to sort this fast!</i> 

To start with, then, there’ll be no more JPEGs; I’ve simply no real use for them (if I ever feel the need, I can pull them as-and-when). 

Then there’s all the existing ones; they’ll be going as well. To make things less laborious, I’ve written a simple script; it works a bit like this: 

1. accept the following as input: camera details; capture date; lens details; event details
2. delete all files with extension JPG
3. prompt for optional archive exclusion of selected files
4. archive all remaining files with extension RAF using the input data for folder structure and filename

That's right; to save as much space as I can, I’ll be squashing the raws to an archive. Here are some stats for reference:

- 32.2 MB for raw (RAF)
- 20.1 MB for 7Zip (7ZP)

just to be cautious, though, I’m excluding any ‘keepers’ (or, at least, keeping external copies).

<br><center><b> To be continued.</b></center><br>





