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

Then I added the following code to convert both still images (including .tiff) and animations (including .apng) to .jxl:

```
[Desktop Entry]
Type=Action
Name=Convert to jxl
Icon=image-jpeg
Profiles=profile-zero;

[X-Action-Profile profile-zero]
MimeTypes=image/*;
Exec=qterminal -e bash -c 'for f in "$@"; do filename=$(basename "$f"); filename="${filename%%.*}"; ext="${f##*.}"; ext_low=$(echo "$ext" | tr "[:upper:]" "[:lower:]"); echo "Processing: $filename"; if [[ "$ext_low" =~ ^(png|apng|gif|jpg|jpeg)$ ]]; then cjxl "$f" "$HOME/Desktop/${filename}.jxl" 2>> "$HOME/Desktop/jxl_error.log"; elif [[ "$ext_low" =~ ^(webp)$ ]]; then tmp="$HOME/Desktop/_tmp_${filename}.png"; ffmpeg -y -i "$f" -pix_fmt rgba -c:v apng "$tmp" 2>> "$HOME/Desktop/jxl_error.log" && cjxl "$tmp" "$HOME/Desktop/${filename}.jxl" 2>> "$HOME/Desktop/jxl_error.log"; rm -f "$tmp"; else tmp="$HOME/Desktop/_tmp_${filename}.png"; ffmpeg -y -i "$f" "$tmp" 2>> "$HOME/Desktop/jxl_error.log" && cjxl "$tmp" "$HOME/Desktop/${filename}.jxl" 2>> "$HOME/Desktop/jxl_error.log"; rm -f "$tmp"; fi; echo "--------------------"; done; echo "All conversions complete!"; read -p "Press Enter to close this window..." dummy' _ %F
Name=Default profile

```

Given the logistics of my current health journey, I needed something to pass the time; as such, I've created a few more right-click wonders (see if you can guess what each of them does): 

- calc-sha.desktop
- view-exif.desktop
- conv-to-html.desktop
- conv-to-md.desktop

I've also created a 'tools menu' with various bash scripts and other useful delights that I'll share the details of shortly.


