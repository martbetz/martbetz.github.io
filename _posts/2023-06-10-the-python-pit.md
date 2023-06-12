---
title: pipx
categories: computing
tags: python
layout: post
---

Need a better installer for Python packages? pipx is a free and open-source application manager that's easy to set up, easy to use, and runs directly from the CLI — _no more ugly version clashes for YOU, my young Bob!_

Installing [Python packages](https://packaging.python.org/en/latest/) with [pip](https://pip.pypa.io/en/stable/) is all well and good; until, that is, it isn't (for reasons we'll discuss another day, installing via pip can potentially lead to system issues further down the line).¹

Using [pipx](https://pypa.github.io/pipx/), packages are conveniently installed in a virtual (sandboxed) environment (think of it as a version of Flatpack that works for Python packages) where all of the hard work (creating the virtual environment, integrating the app within that environment, and adding the app's executable to the user's PATH) is done for you.

If you're running Linux (and why wouldn't you be? 😉), you'll likely find pipx in at least one of your distro's repos; if not (or if the lastest version isn't available), you can find [pipx on pypi](https://pypi.org/project/pipx/). For macOS and Windows users, installation guides are available in the [pipx Github repo](https://github.com/pypa/pipx).

---

¹ Welcome to 'the Python pit,' as I affectionately like to call it. I'll be covering these drawbacks further in a related future post.



