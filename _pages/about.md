---
permalink: /
title: "Ramyad's Website"
redirect_from:
  - /about

feature_row:
  - title: "Invited Talk"
    excerpt: "On-Device Computing: Rain AI's Mission for Energy-Efficient AI Hardware — UCI IAP Workshop, 2024."
    url: "https://vimeo.com/showcase/10699125?video=943465496"
    btn_label: "Watch"
    btn_class: "btn--inverse"
  - title: "PhD Research"
    excerpt: "Managing data in edge systems — guidelines navigating hardware-software trade-offs for next-gen edge."
    url: "/files/overview-website.pdf"
    btn_label: "Overview"
    btn_class: "btn--inverse"
  - title: "Undergrad Research Demos"
    excerpt: "Working closely with 40+ talented undergraduates, resulting in several publications and interactive demos."
    url: "https://sites.gatech.edu/hparch/undergraduate-research/"
    btn_label: "Demo"
    btn_class: "btn--inverse"
---
### [About Me]({% link _pages/about.md %})

I am passionate about unraveling and mastering the complexities of diverse domains. My approach is holistic, integrating various disciplines to craft innovative and comprehensive solutions.  

Currently, at [d-Matrix](https://www.d-matrix.ai/), I am part of the architecture team, advancing the future of ultra-low-latency, sustainable, and commercially viable LLM inference in data centers through the world’s first efficient memory-compute integration. Learn more about me [[here.]]({% link _pages/more_about_me.md %})  


### [Last Entries]({% link _pages/entries.md %})
<ul id="recent-posts" style="list-style-type: none; padding-left: 0">
{% assign entries = site.pages | where_exp: "item", "item.path contains 'entries'" | where_exp: "item", "item.name != 'entries.md'" | sort: 'date' | reverse %}
{% for entry in entries limit:3 %}
  <li><span style="color: gray;">{{ entry.date | date: "%m.%Y" }}</span> - <a href="{{ entry.url | relative_url }}">{{ entry.title }} </a></li>
{% endfor %}
</ul>

### [Selected Work]({% link _pages/portfolio.md %})
{% include feature_row %}
