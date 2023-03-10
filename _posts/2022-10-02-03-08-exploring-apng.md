---
title: Exploring the Potential of APNG
layout: post
categories: photography computing
tags: apng apngasm
---

There's little doubt that when it comes to basic image animation, GIF is is still a solid choice&nbsp;— for the most part, it's easily capable of getting the job done&nbsp;— but for anything more demanding, APNG (at least for now) is likely the better choice.

### Why not use GIFs?

The **G**raphics **I**nterchange **F**ormat has been around forever; it was origionally realeased in 1987&nbsp;— _that's 35 years ago, at the time of writing!_&nbsp;— and has remained a de facto standard ever since. One major drawback of GIFs, however, is that they can only reference a maximum of 256 colours.

###  Why use APNGs?

The **A**nimated **P**ortable **N**etwork **G**raphics format was created in 2004 and is the second-most popular format for animated images to date; unlike GIFs, APNGs can reference up to 16,777,216 colours.¹ Most, _though not all_, web browsers are capable of displaying APNG animations.² 

### How are they made? 

Creating APNGs is a fairly straight forward process (a quick web search will bring up numerous solutions), but unoptimised APNGs can often prove impractical due to their large file size; personally, I use [Max Stepin](https://sourceforge.net/u/maxst/profile)'s  [APNG Assemebler](https://apngasm.sourceforge.net) as it's both easy to install and optimises the files as part of the assembly process.³

---
¹ [JPEG XL is likely the best choice overall](https://martbetz.github.io/photography/computing/2022/10/27/exploring-jpegxl.html), but it's practically unintegrated at the time of writing. caniuse.com provides up-to-date statistics on [JPEG XL browser support](https://caniuse.com/?search=jxl).

² caniuse.com provides up-to-date statistics on [APNG web-browser support](https://caniuse.com/?search=apng).

³ Here's an example of a typical APNG-assembly workflow using APNG Assembler:

  1. create PNG files with (or rename existing PNG files as) `frame0001.PNG`, `frame0002.PNG`, etc.
  2. `CD` into folder containing the files to be assembled
  3. open the command terminal
  4. run command `apngasm -o output-file.apng frame0001.png 5000 frame0002.png 5000`
