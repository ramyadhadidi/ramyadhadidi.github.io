---
permalink: /writings/
title: "Writings"
redirect_from:
  - /writings
  - /posts
  - /blogs
---

<ul id="expandable-list" style="list-style-type: none; padding-left: 0">
{% assign sorted_pages = site.pages | sort: 'date' | reverse %}
{% for page in sorted_pages %}
    {% if page.path contains 'writings' and page.name != 'writings.md' %}
    <li>
      <span style="color: gray;">{{ page.date | date: "%m.%Y" }}</span> - <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
    </li>
    {% endif %}
{% endfor %}
</ul>


