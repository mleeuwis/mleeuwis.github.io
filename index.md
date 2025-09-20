---
title: Home
layout: home
---

# Matto Leeuwis - Biorobotics & Biomechanics

**Jump to:** [News]({{ "/news/" | relative_url }}) - [Projects]({{ "/projects/" | relative_url }}) - [Blog]({{ "/blog/" | relative_url }}) - [CV (PDF)]({{ "/assets/cv/M_CV.pdf" | relative_url }})

---

## News
{% assign items = site.news | sort: "date" | reverse %}
{% if items and items.size > 0 %}
{% for item in items limit:5 %}
- **{{ item.date | date: "%b %-d, %Y" }}** — [{{ item.title }}]({{ item.url | relative_url }})
  {% if item.summary %}
  <br>{{ item.summary }}
  <!-- {% else %}
  <br>{{ item.excerpt | strip_html | truncate: 160 }} -->
  {% endif %}
{% endfor %}
<p><a href="{{ "/news/" | relative_url }}">See all news →</a></p>
{% else %}
_ No news yet. Add files in `_news/` using `YYYY-MM-DD-title.md` _
{% endif %}

---

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
{% endif %}

---

## Recent Blog Posts
{% if site.posts and site.posts.size > 0 %}
{% for post in site.posts limit:3 %}
- **[{{ post.title }}]({{ post.url | relative_url }})**  
  <small>{{ post.date | date: "%b %-d, %Y" }}</small> — {{ post.excerpt | strip_html | truncate: 140 }}
{% endfor %}
<p><a href="{{ "/blog/" | relative_url }}">More posts →</a></p>
{% else %}
_ No posts yet. Add Markdown files in `_posts/` named `YYYY-MM-DD-title.md`. _
{% endif %}