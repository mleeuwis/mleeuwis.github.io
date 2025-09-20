---
layout: page
title: Projects
permalink: /projects/
---

{% assign items = site.projects | sort: 'date' | reverse %}
{% for p in items %}
### [{{ p.title }}]({{ p.url | relative_url }})

{{ p.summary | default: p.excerpt | strip_html }}

*Updated:* {{ p.date | date: site.minima.date_format }}

---
{% endfor %}