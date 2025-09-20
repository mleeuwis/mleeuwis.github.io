---
layout: page
title: Projects
permalink: /projects/
---

{% assign items = site.projects | sort: "date" | reverse %}
{% if items and items.size > 0 %}
{% for p in items %}
### [{{ p.title }}]({{ p.url | relative_url }})

{% if p.collaborators %}- **Authors:** {{ p.collaborators | join: ", " }}{% endif %}
{% if p.tags %}- **Tags:** {{ p.tags | array_to_sentence_string }}{% endif %}
{% if p.status %}- **Status:** {{ p.status }}{% endif %}
{% if p.link %}- **Link:** <a href="{{ p.link }}" target="_blank" rel="noopener">
{% if p.link contains 'doi.org' %}DOI{% else %}External{% endif %}</a>{% endif %}

<!-- {{ p.summary | default: p.excerpt | strip_html }} -->

---
{% endfor %}
{% else %}
_No projects yet — add Markdown files to `/_projects/` with front matter._
{% endif %}