---
title: Posts Related by Tag
layout: page
tag: GIMP
permalink: /tags/GIMP/ # This is only required for pretty links.
---

<div align="left">
    <font size="4">
    This webpage is currently under construction (and until I get out of my rocking chair and do something useful, it’s likely to remain so 😴). When it’s finished (in other words, when I’ve added enough bumf to justify it’s existence), you’ll at least have some hope of finding your way around.
    </font>
</div>

<!-- <hr style="height:0.75px"> -->
<hr style="background-color: #ccc">

<h2>{{ page.tag }}</h2>

<ul>
    {% for post in site.tags[page.tag] %}
    <li>
        <!-- {{ post.date | date: "%B %d, %Y" }}: --> <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>
