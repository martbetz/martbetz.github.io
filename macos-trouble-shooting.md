---
title: macOS Troubleshooting
layout: page
---

---

<font size="4">
<span style="display:block; margin-left:2em; margin-right:2em">
<b>These solutions have worked for me and are listed here for my personal reference only &nbsp;—if you decide to give any of them a go and they solve all of life’s problems, then great; if they don’t, and something catastrophic happens, you’ve no one to blame but yourself.</b>
</span>
</font>

---

## macOS ##

### Issue: ###

- the keyboard shortcut <kbd>CONTROL</kbd> + <kbd>SHIFT</kbd> + <kbd>EJECT</kbd> (put displays to sleep) is no longer available as the keyboard has no <kbd>EJECT</kbd> key

### Solution: ###

- <kbd>CONTROL</kbd> + <kbd>SHIFT</kbd> + <kbd>POWER</kbd>

  or
  
- <kbd>CONTROL</kbd> + <kbd>COMMAND</kbd> + <kbd>Q</kbd>

  (activate lock)

- <kbd>ESCAPE</kbd>

  (turn off displays)

---

## diskutil ##

### Issue: ###

- the free space on a hard-drive needs to be securely erased

### Solution: ###

- `diskutil secureErase freespace [N] /Volumes/[DRIVE]`

  replace [N] with the required value
  
  replace [DRIVE] with the name of the drive
  
### Comments: ###

- the following values can be used for [N]:

    - 0 – single-pass zero-fill erase
    - 1 – single-pass random-fill erase
    - 2 – US DoD 7-pass secure erase
    - 3 – Gutmann algorithm 35-pass secure erase
    - 4 – US DoE algorithm 3-pass secure erase
    
<ul>    
<li>if the name of the drive contains a space, precede it with <code>\</code>; for example, <code>diskutil secureErase freespace 4 /Volumes/Macintosh\ HD</code></li>
</ul>

---

## RansomWhere ##

### Issue: ###

- binaries have been added to the whitelist by default or in error

### Solution: ###

- `sudo /Library/Objective-See/RansomWhere/RansomWhere -reset`

   clear the whitelist and resrt the launch daemon
