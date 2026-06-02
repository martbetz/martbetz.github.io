---
title: Betzy's Actions
layout: page
---

<div>
  <p>
  <center>
    <img style="padding-top: 0px; width:400px;" src="https://raw.githubusercontent.com/martbetz/martbetz.github.io/refs/heads/main/_includes/custom/menu.png" alt="menu">
  </center>
  </p>
</div>

<br>

<!--
<img src="https://github.com/martbetz/martbetz.github.io/blob/main/_includes/custom/Dt.png?raw=true" alt="Centred Image" class="center-block"  style="max-width: 300px; width: 100%; height: auto; margin-left: auto; margin-right: auto"> -->

<font size="4">
<div align="left">

<p style="margin-top: -15px;">
Here's a list of my custom 'right-click' desktop actions that I use with Qterminal and PCManFM-qt as part of the LXqt desktop (I've also included links to any required dependancies). All action files should be made executable and copied to the following location:</p>
</div>
</font>

`/.local/share/file-manager/actions`

<font size="4">
<div align="left">

<p style="margin-top: -15px;">
Where possible, I've tried to keep the executable scripting within the action file; however, there maybe situations in the future where I'll write a seperate script (if complexity demands it).
</p>
</div>
</font>


---

<br>

### calc_sha.desktop ###
Calculates the SHA checksum of a selected file and displays the result in the terminal&nbsp;— a simple and convenient way to quickly validate or share the checksum of any downloaded/uploaded file.

[coreutils (sha256sum)](https://www.gnu.org/software/coreutils/)

<br>

### conv_to_jxl.desktop ###
Converts a selected still or animated image to JPEG XL (.jpx) format&nbsp;— very useful for getting the job done on the fly without having to spin up an image editor or delve into the command line.

[libjxl (cjxl)](https://github.com/libjxl/libjxl); [FFmpeg](https://github.com/FFmpeg/FFmpeg)

<br>

### copy_path.desktop ###
Copies the full path of a selected file to the clipboard&nbsp;— an insanely useful solution that pretty much speaks for itself.

[xclip](https://github.com/astrand/xclip)

<br>

### edit_as_root.desktop ###
Enables a specific file to be edited as Root&nbsp;— a much simpler way to quickly edit files as Root without having to jump into the terminal.

[sudo](https://github.com/sudo-project/sudo?hl=en-GB)

<br>

### view_exif.desktop ###
Displays the exif data of a selected image in the terminal&nbsp;— a quick and light way to view the full EXIF data of any image file right there and then (works great along side a lightweight image viewer such as [FEH](https://github.com/derf/feh)).

[ExifTool](https://github.com/exiftool/exiftool)

<br>

<p style="padding-top: 40px;">
<a class="github-button" href="https://github.com/martbetz/Custom-Actions/tree/main" data-size="large" aria-label="View Repo">View Repo</a>

</p>


