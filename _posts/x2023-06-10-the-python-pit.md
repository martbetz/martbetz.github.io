---
title: pipx
categories: computing
tags: python
layout: post
---

When it comes to Python, installing packages with pip is very common practice; doing so, however, can come at a price. Alternatively, there's pipx: a free and open-source package manager that's purposely designed for the task.

### Why not use pip? ###

[pip](https://pip.pypa.io/en/stable/) installs Python packages directly to the _global system_ Python environment; while this works fine for the short term, problems can arise over time.¹ 

### Why use pipx? ###

[pipx](https://pypa.github.io/pipx/) installs each Python package to a _seperate virtual_ Python environment; as such, this completely removes the potential for any long-term issues. 

### Does this make pipx harder to use? ###

Not at all; pipx is as easy to use as pip. All of the tricky stuff (the creation of environments, the installation of apps, and the setup of executables) is automatically done in the background. 

### Great! Where can I find it? ### 

If you're running Linux (and why wouldn't you be? 😉), you'll likely find a package in your distro's local software repo; if not (or if you prefer), you can either install it from the [pipx pypi repo](https://pypi.org/project/pipx/) or grab the source code directly via the [pipx Github repo](https://github.com/pypa/pipx). pipx is also available for macOS and Windows.

---

¹ Welcome to 'the Python pit,' as I affectionately like to call it. I'll be covering these drawbacks further in a related future post.



