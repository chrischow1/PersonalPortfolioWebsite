---
layout: page
title: Projects
subtitle: "Research prototypes, open-source tools, and applied systems."
permalink: /projects/
---

<div class="card-grid">
  {% for project in site.data.projects %}
  <div class="card">
    <h3>{{ project.name }}</h3>
    <div class="card-meta">{{ project.role }}</div>
    <p>{{ project.description }}</p>
    {% if project.highlights %}
    <ul class="list-plain">
      {% for item in project.highlights %}
      <li>{{ item }}</li>
      {% endfor %}
    </ul>
    {% endif %}
    <div class="tag-list">
      {% for tech in project.tech %}
      <span class="tag">{{ tech }}</span>
      {% endfor %}
    </div>
    <div class="tag-list">
      {% if project.links.github %}<a class="tag alt" href="{{ project.links.github }}">GitHub</a>{% endif %}
      {% if project.links.demo %}<a class="tag alt" href="{{ project.links.demo }}">Demo</a>{% endif %}
      {% if project.links.paper %}<a class="tag alt" href="{{ project.links.paper }}">Paper</a>{% endif %}
    </div>
  </div>
  {% endfor %}
</div>
