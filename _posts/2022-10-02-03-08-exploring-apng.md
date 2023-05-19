---
title: Exploring the Potential of APNG
layout: post
categories: photography computing
tags: apng apngasm
---

When it comes to basic animation, GIF has always been a solid choice; for the most part, it's easily capable of getting the job done. For anything more demanding, though, APNG (at least for now) is likely the best option.

### Why not use GIFs?

The **G**raphics **I**nterchange **F**ormat has been around forever; it was origionally realeased in 1987&nbsp;— _that's 35 years ago, at the time of writing!_&nbsp;— and has remained a de facto standard ever since. A significant limitation of GIFs, however, is that they can only reference a maximum of 256 colours.

### Why use APNGs?¹

The **A**nimated **P**ortable **N**etwork **G**raphics format was created in 2004 and, to date, is the second-most popular format for animated images. APNGs can reference up to 16,777,216 colours, and most modern web browsers are capable of displaying APNG animations.² 

### How are they made? 

Creating APNGs is a fairly straight forward process (a quick web search will bring up numerous solutions), but unoptimised APNGs can often prove impractical due to their large file size; personally, I use [Max Stepin](https://sourceforge.net/u/maxst/profile)'s  [APNG Assemebler](https://apngasm.sourceforge.net) as it's both easy to install and optimises the files as part of the assembly process.³

---
¹ [JPEG XL blows APNG into the weeds](https://martbetz.github.io/photography/computing/2022/10/27/exploring-jpegxl.html), of course, but it's practically unsuppoted at present. caniuse.com provides up-to-date statistics on [JPEG XL browser support](https://caniuse.com/?search=jxl).

² caniuse.com provides up-to-date statistics on [APNG web-browser support](https://caniuse.com/?search=apng).

³ Here's an example of a typical APNG-assembly workflow using APNG Assembler:

  1. create PNG files with (or rename existing PNG files as) `frame0001.PNG`, `frame0002.PNG`, etc.
  2. `CD` into folder containing the files to be assembled
  3. open the command terminal
  4. run command `apngasm -o output-file.apng frame0001.png 5000 frame0002.png 5000`
