---
permalink: /
title: "Ramyad's Website"
redirect_from:
  - /about
---
### [About Me]({% link _pages/about.md %})

At [Rain AI](https://rain.ai/), where we build LLM hardware optimized for the lowest total cost of ownership (TCO), I’m leading workload analysis and benchmarking, high-level SoC analysis, and efficient attention and GEMM mapping techniques on compute units.

I’m a computer architect at heart, but I am ceaselessly intrigued by adjacent areas. I had the opportunity to work on or publish about topics such as processing in and near memory, GPU and CPU architecture, hardware accelerators for machine learning, recommendation systems, sparse problems, and scientific problems, collaborative edge devices, drones, CMOS image sensors, SSDs, and, finally, LLMs. My PhD thesis focused on distributing ML workloads on edge and IoT devices.

Learn more about me [[here.]]({% link _pages/more_about_me.md %})  


### [Last Entries]({% link _pages/entries.md %})
<ul id="recent-posts" style="list-style-type: none; padding-left: 0">
{% assign sorted_pages = site.pages | sort: 'date' | reverse %}
{% for page in sorted_pages limit:3 %}
    {% if page.path contains 'entries' and page.name != 'entries.md' %}
      <li><span style="color: gray;">{{ page.date | date: "%m.%Y" }}</span> - <a href="{{ page.url | relative_url }}">{{ page.title }} </a></li>
    {% endif %}
{% endfor %}
</ul>
