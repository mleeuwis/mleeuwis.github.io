---
layout: page
title: Projects
permalink: /projects/
---

{% assign items = site.projects | sort: "date" | reverse %}
{% if items and items.size > 0 %}
<div class="projects-list">
{% for p in items %}
  <article class="project-row{% unless p.image %} no-thumb{% endunless %}">
    {% if p.image %}
      <a class="project-thumb" href="{{ p.url | relative_url }}">
        <img src="{{ p.image | relative_url }}" alt="{{ p.image_alt | default: p.title }}">
      </a>
    {% endif %}

    <div class="project-text">
      <h3 class="project-title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>

      <p class="project-meta">
        {{ p.date | date: site.minima.date_format }}
        {% if p.status %} · {{ p.status }}{% endif %}
        {% if p.collaborators %} · {{ p.collaborators | join: ", " }}{% endif %}
      </p>

      <p>{{ p.summary | default: p.excerpt | strip_html }}</p>

      {% if p.link %}
        <p><a href="{{ p.link }}" target="_blank" rel="noopener">
          {% if p.link contains "doi.org" %}DOI{% else %}External{% endif %} →
        </a></p>
      {% endif %}
    </div>
  </article>
  <hr>
{% endfor %}
</div>
{% else %}
_No projects yet — add Markdown files to `/_projects/` with front matter._
{% endif %}

{% comment %}
<!-- {% if p.collaborators %}- **Authors:** {{ p.collaborators | join: ", " }}{% endif %}
{% if p.tags %}- **Tags:** {{ p.tags | array_to_sentence_string }}{% endif %}
{% if p.status %}- **Status:** {{ p.status }}{% endif %}
{% if p.link %}- **Link:** <a href="{{ p.link }}" target="_blank" rel="noopener">
{% if p.link contains 'doi.org' %}DOI{% else %}External{% endif %}</a>{% endif %} -->

<!-- {{ p.summary | default: p.excerpt | strip_html }} -->
{% endcomment %}