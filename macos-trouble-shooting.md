---
title: macOS Troubleshooting
layout: page
---

**Disclaimer: These solutions have worked for me and are listed here for my own personal reference. If they work for you too, then great; if they don't, and something catastrophic happens, I won't be held responsible.**

---

### macOS ###

**Issue:**

- Keyboard shortcut `control-shift-eject` (put displays to sleep) is no longer available as the keyboard has no eject key

**Solution:**

- `control-shift-power`

  or
  
   `control-command-Q` followed by `escape`

---

### diskutil ###

**Issue:**

- Free space on HD needs to be securely erased

**Solution:**

- `diskutil secureErase freespace` [n] `/Volumes/`[drive_name]

  replace [n] with one of the following numerical values:

    - 0 – Single-pass zero-fill erase
    - 1 – Single-pass random-fill erase
    - 2 – US DoD 7-pass secure erase
    - 3 – Gutmann algorithm 35-pass secure erase
    - 4 – US DoE algorithm 3-pass secure erase

  replace [drivename] with the name of the drive
