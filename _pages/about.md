---
permalink: /
title: "Ramyad's Website"
redirect_from:
  - /about
---
### [About Me]({% link _pages/about.md %})

I am passionate about unraveling and mastering the complexities of diverse domains. My approach is holistic, integrating various disciplines to craft innovative and comprehensive solutions.

Currently, at [Rain AI](https://rain.ai/), we are creating a future with abundant and scalable artificial intelligence. We're building the world’s most cost and energy efficient hardware for AI. My role revolves around AI accelerator architecture design, ML hardware-software co-design, LLMs, workload analysis, path finding, profiling and competitive analysis, and technical customer interaction. Learn more about me [[here.]]({% link _pages/more_about_me.md %})  


### [Last Entries]({% link _pages/entries.md %})
<ul id="recent-posts" style="list-style-type: none; padding-left: 0">
{% assign sorted_pages = site.pages | sort: 'date' | reverse %}
{% for page in sorted_pages limit:3 %}
    {% if page.path contains 'entries' and page.name != 'entries.md' %}
      <li><span style="color: gray;">{{ page.date | date: "%m.%Y" }}</span> - <a href="{{ page.url | relative_url }}">{{ page.title }} </a></li>
    {% endif %}
{% endfor %}
</ul>
