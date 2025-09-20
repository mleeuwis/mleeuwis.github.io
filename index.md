---
title: Home
layout: home
---

I study human movement through the lens of robotics, biomechanics, and sensorimotor neuroscience. My work explores how the nervous system interacts with the body and environment to generate skilled, adaptable behavior. Using tools such as a robotic balance simulator, I investigate how humans learn altered control dynamics, ranging from small perturbations to the complete reversal of postural control. In parallel, I use musculoskeletal models to simulate and measure the energetic cost of human posture and gait, aiming to determine whether simple models accurately describe human movement and physiology. In other applied work, I developed a dynamic model of a wheelchair that could be pushed from the side for improved social interaction. By examining motor control from a dynamic systems perspective, I aim to uncover fundamental principles in biological or engineered systems that enable us to move with intelligence and purpose.

---

## News
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


<!-- ---

## Featured Projects
{% assign projs = site.projects | sort: "date" | reverse %}
{% if projs and projs.size > 0 %}
{% for p in projs limit:3 %}
### [{{ p.title }}]({{ p.url | relative_url }})
{{ p.summary | default: p.excerpt | strip_html | truncate: 180 }}

{% endfor %}
<p><a href="{{ "/projects/" | relative_url }}">All projects →</a></p>
{% else %}
_ No projects yet. Add files in `_projects/` with a `summary:` in the front matter. _
{% endif %} -->

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