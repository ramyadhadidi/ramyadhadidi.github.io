---
permalink: /
title: "Ramyad's Website"
excerpt: ""
redirect_from:
  - /about
---
### About Me

With a breadth of knowledge spanning a multitude of related domains, I thrive on understanding the big picture and deconstruct complex systems. My approach involves intricately weaving the threads of distinct fields to build comprehensive and innovative solutions.

Currently, I am shaping the future of edge computing at [Rain](https://rain.ai/), a company that harnesses low-power, robust training, and high-performing inference capabilities akin to artificial brains. [[...more]]({% link _pages/more_about_me.md %})


### [Entries]({% link _pages/entries.md %})

<ul id="recent-posts" style="list-style-type: none; padding-left: 0">
{% assign sorted_pages = site.pages | sort: 'date' | reverse %}
{% for page in sorted_pages limit:5 %}
    {% if page.path contains 'entries' and page.name != 'entries.md' %}
    <li>
      <span style="color: gray;">{{ page.date | date: "%m.%Y" }}</span> - <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
    </li>
    {% endif %}
{% endfor %}
</ul>
