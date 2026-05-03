---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

Peer-reviewed research from graduate work at the University of Louisville's
[Louisville Automation and Robotics Research Institute (LARRI)](https://engineering.louisville.edu/research/centers-institutes/larri/).

**Google Scholar metrics:** 23 total citations &middot; h-index 3 &middot; i10-index 1
&nbsp;&nbsp; [Full profile &rarr;](https://scholar.google.com/citations?user=xLFRTm0AAAAJ&hl=en)

---

{% assign by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for group in by_year %}
## {{ group.name }}

{% for pub in group.items %}
**{{ pub.title }}**  
{{ pub.authors }}  
*{{ pub.venue }}*{% if pub.volume %}, {{ pub.volume }}{% endif %}  
{{ pub.role }}{% if pub.citations %} &middot; {{ pub.citations }} citations{% endif %}{% if pub.url %} &middot; [Full text &rarr;]({{ pub.url }}){% endif %}

{% endfor %}
{% endfor %}
