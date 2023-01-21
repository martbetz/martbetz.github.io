---
title: Exploring the Potential of JXL
layout: post
categories: photography computing
---

For as long as there's been digital photography, there's been JPEG — _it's been the standard digital photo format for over 30 years!_ — but its direct sucessor, JPEG XL, is finally here (and it could even replace PNG and GIF, too).

### Why replace JPEG? ###

The **J**oint **P**hotographic **E**xprts **G**roup format has been a mainstay of digital imagery since 1992; however, despite its unprecedented popularity, it's never really offered a _complete_ solution for digital photographers. 

### How does JPEG XL address this? ###

The **J**oint **P**hotographic **E**xprts **G**roup **X** **L**ong-Term format (_WTF?!_ 🤢) brings _a lot_ of new features to the table: support for wide colour gamuts and high bit-depths, alpha channel and multi-layer image support, lossless compression, and advanced lossy compression and progressive decoding.¹

### How do the results compare? ###

The following chart shows the comparative file sizes when following my typical workflow. In order to create and display the JXLs, I installed the [qt6-jpegxl-image-plugin](https://aur.archlinux.org/packages/qt6-jpegxl-image-plugin) from the AUR.² I used an intermediate TIF as both a reference point and as a  'stepping stone' between RawTherapee and Krita.³


<div align="center">
<p>
 <img style="padding-top: 15px; padding-bottom: 20px;" src="https://raw.githubusercontent.com/martbetz/martbetz.github.io/main/_includes/custom/jxl-chart1.png" alt="File-Size Compariston Test Chart">
</p>
</div>

For my typical use case (blue), the difference in file size was 1.42 MB — _that's a reduction of over 60%!_ Likewise, when compared to PNG (red), the difference in file size was 1.68 MB — _an equally  impressive reduction of 43%!_ 

It's also worth noting the comparison between the JPG and the _lossless_ JXL, the later being 0.16MB smaller than the former — _in other words, the lossless JPEG XL is almost 7% lighter than the lossy JPEG!_ 

As far as image quality goes, I could see no discernible difference right accross the board (no surprises here, though, given that the highest quality settings were used for both the JPEG and the lossy JPEG XL).

### When will adoption role out? ###

JPEG XL has already been finalised, but it could take a while before it gains traction; none of the popular web browsers support it just yet (at least, not by default), but here's to hoping that changes very soon.⁴ ⁵



---
¹ wikipedia.com provides a comprehensive list of [JPEG XL features](https://en.m.wikipedia.org/wiki/JPEG_XL#Features).

² My weapon of choice is KDE Manaro, so this was a no-brainer; in less than two minutes, support was added to _all_ my KDE apps — _as well as [GIMP](https://www.gimp.org/), and even my beloved [feh](https://feh.finalrewind.org)!_ 😍️ 

³ I could have just used the PNG, of course, but then my chart wouldn't have looked anywhere near as pretty! 😉

⁴ caniuse.com provides up-to-date statistics on [JPEG XL browser support](https://caniuse.com/?search=jxl). 

⁵ And yet, just as I finished writing this post, _[Google dropped support for JPEG XL in Chromium](https://cloudinary.com/blog/the-case-for-jpeg-xl)!_ 😠
