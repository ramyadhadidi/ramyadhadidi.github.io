---
permalink: /
title: "Ramyad's Website"
redirect_from:
  - /about
---
### [About Me]({% link _pages/about.md %})

I am passionate about unraveling and mastering the complexities of diverse domains. My approach is holistic, integrating various disciplines to craft innovative and comprehensive solutions.  

Currently, at [d-Matrix](https://www.d-matrix.ai/), I am part of the architecture team, advancing the future of ultra-low-latency, sustainable, and commercially viable LLM inference in data centers through the world’s first efficient memory-compute integration. Learn more about me [[here.]]({% link _pages/more_about_me.md %})  


### [Last Entries]({% link _pages/entries.md %})
<ul id="recent-posts" style="list-style-type: none; padding-left: 0">
{% assign sorted_pages = site.pages | sort: 'date' | reverse %}
{% for page in sorted_pages limit:3 %}
    {% if page.path contains 'entries' and page.name != 'entries.md' %}
      <li><span style="color: gray;">{{ page.date | date: "%m.%Y" }}</span> - <a href="{{ page.url | relative_url }}">{{ page.title }} </a></li>
    {% endif %}
{% endfor %}
</ul>

<!-- Project examples
- Talk UIAP
- Academic Package + slides
- Drone Talk
- DAC research talk
- Demos ()
  - https://hparch.gatech.edu/fpl19/)
  - https://hparch.gatech.edu//sysml
  - https://ramyadhadidi.github.io/files/hadidi-Edge-2023-Context-Aware-Drone-Example-Video.mp4 -->
