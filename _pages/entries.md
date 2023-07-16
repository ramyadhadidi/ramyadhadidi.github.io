---
permalink: /entries/
title: "Entries"
redirect_from:
  - /entries
  - /posts
  - /blogs
---

<ul id="expandable-list" style="list-style-type: none; padding-left: 0">
{% assign sorted_pages = site.pages | sort: 'date' | reverse %}
{% for page in sorted_pages %}
    {% if page.path contains 'entries' and page.name != 'entries.md' %}
    <li>
      <span style="color: gray;">{{ page.date | date: "%m.%Y" }}</span> - <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
    </li>
    {% endif %}
{% endfor %}
</ul>


