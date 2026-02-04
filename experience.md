---
layout: page
title: Experience
subtitle: "Academic positions, industry internships, and leadership roles."
permalink: /experience/
---

<div class="card-grid">
  {% for role in site.data.experience %}
  <div class="card">
    <h3>{{ role.role }}</h3>
    <div class="card-meta">{{ role.org }} | {{ role.start }} - {{ role.end }} | {{ role.location }}</div>
    <p>{{ role.summary }}</p>
    {% if role.bullets %}
    <ul class="list-plain">
      {% for item in role.bullets %}
      <li>{{ item }}</li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
  {% endfor %}
</div>
