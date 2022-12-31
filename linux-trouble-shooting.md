---
title: Linux (Arch) Troubleshooting
layout: page
---

**Disclaimer: These solutions have worked for me and are listed here for my personal reference only. If you decide to give any of them a go and they solve all of life's problems, then great; if they don't, and something catastrophic happens, you've no one to blame but yourself. Once again: these solutions are listed here for my personal reference only!**

---

### pacman/pamac ###

**Issue:**

- A package from the AUR failed because pgp signature(s) could not be varified.

**Solution:**

- `gpg --recv-keys` [SIG]

   Replace [SIG] with the signature to be added.

**Comments:**

- [pacman cheat-sheet](https://difyel.com/cheatsheet/pacman-cheat-sheet/index.html)

----

### python-pip ###

**Issue:**

- `ValueError: bad marshal data (unknown type code)`

   (corrupt/incompatible *.pyc file/files)

**Solution:**

- `find /usr -name '*.pyc' -delete`

   (find and delete all *.pyc files)

- `pacman -S python-pip` / `pamac install python-pip`

   (re-install python-pip)

**Comments:**

- Deleting all *.pyc files will subsequently remove any corrupted/incompatible *.pyc files. Re-installing python-pip will create a new batch of *.pyc files that will replace those previously deleted.

----

### git ###

**Issue:**

 - A previous commit comment is incorrect and needs to be amended

**Solution:**

- `git log --oneline --graph`

  (list commits to identify SHA)

- `git rebase -i` [SHA]

Replace [SHA] with the SHA of the commit that immediately _**proceeds**_ the comment to be amended.

- For the comment to be amended, replace the keyword `pick` with the keyword `reword`. Save the file and exit the editor.

- Amend the commit comment and save the file.

- `git log --oneline --graph`

  (list commits to review changes)

**Comments:**

- An alternative and _much_ quicker solution would be to use the 'reword' option in `laygit`.

----  
  
 ### git ###
  
 **Issue:**
  
 - The latest commit is incorrect and needs to be removed.
  
  **Solution:**
  
 - `git reset --hard HEAD^`
  
 - (delete the latest commit and revert to the previous state)
 
 ---- 

### clamav ###

**Issue:**

- Signatures fail to update.

**Solution:**

- `sudo rm /var/lib/clamav/*.*`

   (remove contents of the 'clamav' directory)

- `sudo freshclam`

   (update signatures)
   
- `sudo clamscan -r -i / > clamav.log `

   (run full recursive system scan, list positives only, and output results to a text file named 'clamav.log')
   
**Comments:**

- Windows executables and file wrappers (used with Wine, for example) may produce false positives.

----

### gimp ###

**Issue:**

- Python modules have been removed from the official repository package resulting in Python scripts and plug-ins (such as Resynthesizer) being unsupported and the Python-Fu console becoming unavailable.

**Solution:**

- `pamac install python2-gimp`
  
    (install the Python support modules from the AUR)
    
**Comments:**
    
- Pamac AUR support _must_ be enabled.

----

### fiejail ###

**Issue:**

- Apps do not run via firefjail by default.

**Solution:**

- `ln -s /usr/bin/firejail /usr/local/bin/`[appname]

   Repace [appname] with the name of the app.
   
   (create a symbolic link for a specific app)
   
   **or:**

- `sudo firecfg`

    (create symbolic links to all sandboxed apps)
    
- `cd /usr/local/bin`

    (navigate to directory where symbolic links have been created)
    
-  `sudo rm -v !("`[appname1]`"|"`[appname2]`")`

   Repace [appname1] and [appname2] with the names of the apps.

    (delete all symbolic links except those required)
    
**Comments:**
    
- firecfg is the desktop integration utility for firejail - it allows the user to sandbox applications automatically by clicking on desktop manager icons and menus).

- `sudo firecfg --clean` will delete all created symbolic links.

----

### FFmpeg ###

**Issue:**

- 30fps action cam footage needs to be converted to a lower framerate.

**Solution:**

- [30fps.MOV] `-vf minterpolate=mi_mode=mci:mc_mode=aobmc:me_mode=bidir:vsbmc=1:fps=50,decimate=cycle=2,format=pix_fmts=yuvj420p -c:v libx264 -preset veryslow -tune film -crf 17` [25fps.MOV]
 
**Comments:**

- Set `fps=` value to twice the desired framerate (for example, set `fps=50` for 25fps or `fps=48` for 24fps).
