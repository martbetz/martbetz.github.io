---
layout: page
tag: diy
permalink: /tags/diy/ # This is only required for pretty links.
# Thus, this page's link is /tags/jekyll/ rather than /tags/jekyll.html
---

<h3>{{ page.tag | capitalize }}</h3>

<ul>
    {% for post in site.tags[page.tag] %}
    <li>
        <!-- {{ post.date | date: "%B %d, %Y" }}: --> <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>
