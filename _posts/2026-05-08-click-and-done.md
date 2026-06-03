---
title: Click and Done
layout: post
categories: computing photography
---

I really do like a simple life. I needed an easy way of converting a single image file directly to JPEG XL without having to load up an image editor or play around in the terminal&nbsp;— so I went away and created one.

In my case, I'm running LX-qt on Arch (which means the menu entries are handled by PCManFM-qt, the lifting is done by cjxl and ffmpeg, and the output is displayed in Qterminal).

Firstly, I created the custom action file as follows:

```
mkdir -p ~/.local/share/file-manager/actions && \
cat << 'EOF' > ~/.local/share/file-manager/actions/conv-to-jxl.desktop
```

Then I added [the code](https://raw.githubusercontent.com/martbetz/Custom-Actions/refs/heads/main/conv_to_jxl.desktop) to convert both still images (including .tiff) and animations (including .apng).

Given the logistics of my current health journey, I needed something to pass the time; as such, I've created a few more [right-click wonders](https://martbetz.github.io/betzys-custom-actions.html) (see if you can guess what each of them does&nbsp;😉).

I've also created a 'tools menu' with various bash scripts and other useful delights that I'll share the details of shortly.


