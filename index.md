---
layout: default
title: Home
---

<section class="hero">
  <div class="hero-card">
    <p class="eyebrow">Researcher · Builder · Collaborator</p>

    <h1>{{ site.profile.name }}</h1>

    <p class="lead">
      {{ site.profile.title }} at {{ site.profile.affiliation }}.
      I focus on building reliable, efficient, and real-world engineering systems.
    </p>

    <div class="hero-actions">
      <a class="btn btn-primary" href="{{ '/resume/' | relative_url }}">Download Resume</a>
      <a class="btn btn-ghost" href="mailto:{{ site.profile.email }}">Email</a>
      {% if site.profile.linkedin %}
      <a class="btn btn-ghost" href="{{ site.profile.linkedin }}" target="_blank">LinkedIn</a>
      {% endif %}
      {% if site.profile.github %}
      <a class="btn btn-ghost" href="{{ site.profile.github }}" target="_blank">GitHub</a>
      {% endif %}
    </div>

    <div class="callout">
      Open to internships, research opportunities, and industry collaborations.
      Reach me at <a href="mailto:{{ site.profile.email }}">{{ site.profile.email }}</a>.
    </div>
  </div>

  <aside class="hero-card profile-card">
    {% if site.profile.headshot %}
    <img src="{{ site.profile.headshot | relative_url }}" alt="Headshot">
    {% endif %}

    <div class="profile-meta">
      {% if site.profile.location %}
      <div><strong>Location:</strong> {{ site.profile.location }}</div>
      {% endif %}

      {% if site.profile.education %}
      <div><strong>Education:</strong> {{ site.profile.education }}</div>
      {% endif %}

      {% if site.profile.phone %}
      <div><strong>Phone:</strong> {{ site.profile.phone }}</div>
      {% endif %}
    </div>
  </aside>
</section>


<section class="section">
  <div class="section-title">
    <h2>Featured Projects</h2>
    <a href="{{ '/projects/' | relative_url }}">View all</a>
  </div>

  {% if site.data.projects %}
  <div class="card-grid">
    {% for project in site.data.projects limit:2 %}
    <div class="card">
      <h3>{{ project.name }}</h3>
      <div class="card-meta">{{ project.role }}</div>
      <p>{{ project.description }}</p>

      {% if project.tech %}
      <div class="tag-list">
        {% for tech in project.tech %}
        <span class="tag">{{ tech }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
  {% else %}
  <p>Add project entries in <code>_data/projects.yml</code>.</p>
  {% endif %}
</section>


<section class="section">
  <div class="section-title">
    <h2>Recent Experience</h2>
    <a href="{{ '/experience/' | relative_url }}">View all</a>
  </div>

  {% if site.data.experience %}
  <div class="card-grid">
    {% for role in site.data.experience limit:2 %}
    <div class="card">
      <h3>{{ role.role }}</h3>
      <div class="card-meta">
        {{ role.org }} | {{ role.start }} - {{ role.end }}
      </div>
      <p>{{ role.summary }}</p>
    </div>
    {% endfor %}
  </div>
  {% else %}
  <p>Add experience entries in <code>_data/experience.yml</code>.</p>
  {% endif %}
</section>
