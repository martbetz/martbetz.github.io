---
title: pipx
categories: computing
tags: python
layout: post
---

When it comes to Python, installing packages with pip is very common practice; doing so, however, can come at a price. Alternatively, there's pipx: a free and open-source package manager that's purposely designed for the task.

### Why not use pip? ###

[pip](https://pip.pypa.io/en/stable/) installs Python packages directly to the main system Python environment; while this works fine for the short term, problems can arise over time.¹ 

### Why use pipx? ###

[pipx](https://pypa.github.io/pipx/) installs each Python package to a seperate virtual Python environment; in turn, this completely removes the potential for any long-term issues. 

### Sounds complicated! ###

Au contraire, my dear Bob; all of the hard work (the creation of environments, the installation of apps, and the setup of executables) is automatically done in the background.

### Great! Where can I find it? ###

If you're running Linux (and why wouldn't you be? 😉), you'll likely find pipx in at least one of your distro's repos; if not (or if the lastest version isn't available), you can find [pipx on pypi](https://pypi.org/project/pipx/). For macOS and Windows users, installation guides are available in the [pipx Github repo](https://github.com/pypa/pipx).

---

¹ Welcome to 'the Python pit,' as I affectionately like to call it. I'll be covering these drawbacks further in a related future post.



