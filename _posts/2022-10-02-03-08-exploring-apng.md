---
title: Exploring APNG
layout: post
categories: photography computing
---

When it comes to basic web animation, GIF has always been a solid choice; for the most part, it's easily capable of getting the job done. For anything more demanding, though, APNG (at least for now) is likely the best option.

### Why _not_ use GIFs?

The **G**raphics **I**nterchange **F**ormat has been around forever; it was origionally realeased in 1987&nbsp;— _that's 35 years ago, at the time of writing!_&nbsp;— and has remained a de facto standard ever since. GIFs, however, are significantly limited in flexibility; they can only reference a maximum of 256 colours.

### Why use APNGs?¹

The **A**nimated **P**ortable **N**etwork **G**raphics format was created in 2004 and, to date, is the second-most popular format for animated images. APNGs can reference up to 16,777,216 colours, and most modern web browsers are capable of displaying APNG animations.² 

### How are they made? 

Creating APNGs is a fairly straight forward process (a quick web search will bring up numerous solutions), but unoptimised APNGs can often prove impractical due to their large file size; personally, I use [Max Stepin](https://sourceforge.net/u/maxst/profile)'s  [APNG Assemebler](https://apngasm.sourceforge.net) as it's both easy to install and optimises the files as part of the assembly process.³

<p style="padding-top: 15px; line-height: 1.1">
<font size="2">
¹ While <a href="https://martbetz.github.io/photography/computing/2022/10/27/exploring-jpegxl.html">the potential of JPEG XL</a> blows APNG into the weeds (along with everything else for that matter), it’s yet to be widely adopted. (caniuse.com provides up-to-date sdtatistics on <a href="https://caniuse.com/?search=jxl">JPEG XL browser support</a>).
</font>
</p>

<p style="padding-top: -5px; line-height: 1.1">
<font size="2">
² caniuse.com provides up-to-date statistics on <a href="https://caniuse.com/?search=apng">APNG browser support</a>.
</font>
</p>

<p style="padding-top: -5px; line-height:1.1">
<font size="2">
³ Here’s an example of a typical APNG-assembly workflow using APNG Assembler:
</font>
</p>


<p style="padding-top: -5px; line-height:1.25">
<font size="2">
<ol>
<li>create PNG files with (or rename existing PNG files as) <code>frame0001.PNG</code>, <code>frame0002.PNG</code>, etc.</li>
<li><code>CD</code> into folder containing the files to be assembled</li>
<li>open the command terminal</li>
<li>run command <code>apngasm -o output-file.apng frame0001.png 5000 frame0002.png 5000</code></li>
</ol>
</font>
</p>
