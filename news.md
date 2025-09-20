---
layout: page
title: News
permalink: /news/
---


{% assign items = site.news | sort: 'date' | reverse %}
<ul>
{% for item in items %}
<li>
<span>{{ item.date | date: site.minima.date_format }}</span> —
<a href="{{ item.url | relative_url }}">{{ item.title }}</a>
</li>
{% endfor %}
</ul>