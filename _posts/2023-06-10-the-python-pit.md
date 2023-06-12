---
title: pipx
categories: computing
tags: python
layout: post
---

Looking for a better way of installing Python packages? pipx is a free and open-source application manager that's easy to use and runs directly from the CLI — _no more pesky version clashes for you, then, Bob!_

Installing [Python packages](https://packaging.python.org/en/latest/) with [pip](https://pip.pypa.io/en/stable/) is all well and good; until, that is, it isn't (for reasons that'll be discussed another day, this approach could potentially lead to system issues further down the line). 

Using [pipx](https://pypa.github.io/pipx/), packages are conveniently installed in a virtual (sandboxed) environment (think of it as a version of Flatpack that works for Python packages) where all of the hard work (creating the virtual environment, integrating the app within that environment, and adding the app's executable to the user's PATH) is done for you.

If you're running Linux (and why wouldn't you be? 😉), you'll likely find pipx in your distro's repo(s); if not (or if the repo version's outdated), you can find [pipx on pypi](https://pypi.org/project/pipx/). For macOS and Windows users, installation guides are available in the [pipx Github repo](https://github.com/pypa/pipx).



