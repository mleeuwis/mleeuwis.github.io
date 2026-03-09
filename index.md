---
title: Home
layout: home
---

<div style="display: flex; flex-wrap: wrap; align-items: center; gap: 1.5rem;">

  <div style="flex: 0 0 300px; text-align: center;">
    <img src="{{ '/assets/images/home-image-robot.jpg' | relative_url }}"
         alt="Balance experiment figure"
         style="max-width: 100%; height: auto; border-radius: 8px;">
  </div>
  
  <div style="flex: 1 1 300px;">
    <p>
      I'm a PhD student at the 
      <a href="https://neuro.nl/research/forbes" target="_blank" rel="noopener">
      Sensorimotor Neuroscience and Biorobotics Lab
      </a> 
      in Erasmuc MC (Rotterdam).
      My work focuses on human movement and learning through the lens of 
      <a href="{{ '/projects/conditioning/' | relative_url }}">robotics</a>, 
      <a href="{{ '/projects/energy-expenditure-standing-gait/' | relative_url }}">biomechanics</a>, 
      and <a href="{{ '/projects/inversions/' | relative_url }}">neuroscience</a>.
      Before doing my PhD I studied Mechanical Engineering at TU Delft, where we designed a 
      <a href="{{ '/projects/wheelchair-ziggy/' | relative_url }}">wheelchair</a>
      that could be pushed from the side.
    </p>
  </div>
</div>

<br>

---

# News
{% assign items = site.news | sort: "date" | reverse %}
{% if items and items.size > 0 %}
<ul class="news-list">
{% for item in items limit:5 %}
  <li>
    <strong>{{ item.date | date: "%Y-%m-%d" }}</strong> —
    {% if item.link %}
      <a href="{{ item.link }}" target="_blank">{{ item.title }}</a>
    {% else %}
      {{ item.title }}
    {% endif %}
  </li>
{% endfor %}
</ul>
<p><a href="{{ "/news/" | relative_url }}">See all news →</a></p>
{% else %}
<p><em>No news yet. Add files in `_news/` using `YYYY-MM-DD-title.md`</em></p>
{% endif %}


---

# Featured Projects
{% assign projs = site.projects | sort: "date" | reverse %}
{% if projs and projs.size > 0 %}
{% for p in projs limit:2 %}
### [{{ p.title }}]({{ p.url | relative_url }})
{{ p.summary | default: p.excerpt | strip_html | truncate: 180 }}

{% endfor %}
<p><a href="{{ "/projects/" | relative_url }}">All projects →</a></p>
{% else %}
_ No projects yet. Add files in `_projects/` with a `summary:` in the front matter. _
{% endif %}

---

<!-- ## Recent Blog Posts
{% if site.posts and site.posts.size > 0 %}
{% for post in site.posts limit:3 %}
- **[{{ post.title }}]({{ post.url | relative_url }})**  
  <small>{{ post.date | date: "%b %-d, %Y" }}</small> - {{ post.excerpt | strip_html | truncate: 140 }}
{% endfor %}
<p><a href="{{ "/blog/" | relative_url }}">More posts →</a></p>
{% else %}
_ No posts yet. Add Markdown files in `_posts/` named `YYYY-MM-DD-title.md`. _
{% endif %} -->