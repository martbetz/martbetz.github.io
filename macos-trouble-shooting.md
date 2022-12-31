---
title: macOS Troubleshooting
layout: page
---

<font size="4">
<b>Disclaimer: These solutions have worked for me and are listed here for my personal reference only. If you decide to give any of them a go and they solve all of life's problems, then great; if they don't, and something catastrophic happens, you've no one to blame but yourself. Once again: these solutions are listed here for my personal reference only!</b>
</font>

---

### macOS ###

**Issue:**

- the keyboard shortcut `control-shift-eject` (put displays to sleep) is no longer available as the keyboard has no eject key

**Solution:**

- `control-shift-power`

  or
  
- `control-command-Q` followed by `escape`

---

### diskutil ###

**Issue:**

- the free space on a hard-drive needs to be securely erased

**Solution:**

- `diskutil secureErase freespace` [n] `/Volumes/`[drive_name]

  replace [drivename] with the name of the drive

  replace [n] with one of the following numerical values:

    - 0 – Single-pass zero-fill erase
    - 1 – Single-pass random-fill erase
    - 2 – US DoD 7-pass secure erase
    - 3 – Gutmann algorithm 35-pass secure erase
    - 4 – US DoE algorithm 3-pass secure erase
    

  
  
