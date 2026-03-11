---
layout: page
title: News and updates
permalink: /news/
---

{% assign items = site.news | sort: "date" | reverse %}
<ul class="news-list">
{% for n in items %}
  <li>
    <strong>{{ n.date | date: "%Y-%m-%d" }}</strong> ·
    {% if n.link %}
      <a href="{{ n.link }}" target="_blank">{{ n.title }}</a>
    {% else %}
      {{ n.title }}
    {% endif %}
  </li>
{% endfor %}
</ul>