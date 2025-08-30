---
title: Waste of Space
layout: post
categories: photography computing
---

So here I am, over a decade later, pouting over wasted disk space and thinking “What?! JPEG <i>and</i> raw?! <i>Why on Earth am I doing that?!</i>” At least I’ve found the solution: stop it —&nbsp;<i>right now!</i>&nbsp;— and bin those pesky JPEGs! 😶

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

That's right; to save as much space as I can, I’ll be squashing the raws to an archive. Here are some expected ball-park stats:

- 32.2 MB for raw (RAF)
- 20.1 MB for 7Zip (7ZP)

just to be cautious, though, I’m excluding any ‘keepers’ (or, at least, keeping external copies).

<hr>

Update (Feb 15, 2025): We’ll, I’m off to a flying start with 168 GB reclaimed on a 500 GB drive. All the surplus JPEGs have gone (and a sack load of other stuff, too), and I’ve not squashed anything down just yet! 

I’ve also been pondering my folder tree. After much deliberation, I’ve decided on the following:

- camera details (e.g. Fuji_XT10)
- lens details (e.g. Fuji_XC_35mm)
- event details (e.g. Street-London-2020)
- capture date (e.g. 01-01-2020)

The structure is simple and seems to work well (I wanted to keep nesting to a minimum and the folder names short yet descriptive). 

<hr>

Update (Feb 18, 2025): Now that I’ve sorted the main drive, I’m doing the same for the spare; this one’s a bit of a junk draw, where all my old photos are dumped. I think I’ll be here for a while — <i>wish me luck!</i>

<hr>

Update (Feb 19, 2025): I’m still hard at it; another five hours put in today, and I’m roughly half-way there. My only error so far was the way I named the subs; had the dates been tagged in reverse (YYYY-MM-DD) they’d be far less taxing to sort — <i>Aaawww... I gone and done a stoopid, Bob! Why I do a stoopid?!</i>&nbsp;😣

<hr>

Update (Feb 20, 2025): And... we’re done! Everthing’s been sorted and fully backed up to a second drive. 

As it turned out, I decided not to compress any raw files; it all came in at around 400 GB, which is more than acceptable for now. What I’ve decided to do instead is manage it all with <a href="https://www.kphotoalbum.org/">KPhotoAlbum</a>; it’s all set up, and I have a plan. 😁

As one of the archives will remain workable, I’ve tweaked my RawTherapee settings to only store the sidecar files in the cache folder; this will help make sure that everything stays as clutter free as possible.

<br><center><b> To be continued.</b></center><br>





