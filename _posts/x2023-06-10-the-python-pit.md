---
title: pipx
categories: computing
tags: python
layout: post
---

Need a better installer for Python packages? pipx is a free and open-source application manager that's easy to set up, easy to use, and runs directly from the CLI — _no more ugly version clashes for YOU, my young Bob!_

<h2>Why not install using pip?</h2>

Installing [Python packages](https://packaging.python.org/en/latest/) with [pip](https://pip.pypa.io/en/stable/) is all very well and good; until, that is, it isn't — _while everything works fine in the short term, problems can arise over time._ ¹ 

<h2>Why use pipx?</h2>

[pipx](https://pypa.github.io/pipx/) installs each and every Python package within its own virtual environment; in turn, this completely removes the potential for such longer-term issues. 

<h2>Great! Where can I find it?</h2>

If you're running Linux (and why wouldn't you be? 😉), you'll likely find pipx in at least one of your distro's repos; if not (or if the lastest version isn't available), you can find [pipx on pypi](https://pypi.org/project/pipx/). For macOS and Windows users, installation guides are available in the [pipx Github repo](https://github.com/pypa/pipx).

---

¹ Welcome to 'the Python pit,' as I affectionately like to call it. I'll be covering these drawbacks further in a related future post.



