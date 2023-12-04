---
permalink: /
title: "Ramyad's Website"
excerpt: ""
redirect_from:
  - /about
---
### About Me

I am passionate about unraveling and mastering the complexities of diverse domains. My approach is holistic, integrating various disciplines to craft innovative and comprehensive solutions.  

Currently, at [Rain](https://rain.ai/), I am at the forefront of edge computing, contributing to the development of artificial brain-like systems characterized by low-power usage, efficient training, and high-performance inference capabilities. Learn more about my journey [[...here]]({% link _pages/more_about_me.md %})  


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
