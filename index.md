---
layout: default
title: Home
---

<section class="hero">
  <div class="hero-card">
    <p class="eyebrow">Researcher · Builder · Collaborator</p>
    <h1>{{ site.profile.name }}</h1>
    <p class="lead">
      {{ site.profile.title }} at {{ site.profile.affiliation }}. I design and deploy
      human-centered AI systems with an emphasis on reliability, interpretability, and
      real-world impact.
    </p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="{{ '/resume/' | relative_url }}">Download CV</a>
      <a class="btn btn-ghost" href="mailto:{{ site.profile.email }}">Email</a>
      <a class="btn btn-ghost" href="{{ site.profile.scholar }}">Scholar</a>
    </div>
    <div class="callout">
      Open to research collaborations, speaking invitations, and industry partnerships.
      Reach me at <a href="mailto:{{ site.profile.email }}">{{ site.profile.email }}</a>.
    </div>
  </div>
  <aside class="hero-card profile-card">
    <img src="{{ site.profile.headshot | relative_url }}" alt="Headshot">
    <div class="profile-meta">
      <div><strong>Location:</strong> {{ site.profile.location }}</div>
      <div><strong>Website:</strong> <a href="{{ site.profile.website }}">{{ site.profile.website }}</a></div>
      <div><strong>GitHub:</strong> <a href="{{ site.profile.github }}">{{ site.profile.github }}</a></div>
      <div><strong>Scholar:</strong> <a href="{{ site.profile.scholar }}">{{ site.profile.scholar }}</a></div>
    </div>
    <div class="tag-list">
      <span class="tag">LLMs</span>
      <span class="tag">HCI</span>
      <span class="tag">ML Systems</span>
      <span class="tag alt">Retrieval</span>
    </div>
  </aside>
</section>

<section class="section">
  <div class="section-title">
    <h2>Research Snapshot</h2>
  </div>
  <div class="stats-grid">
    <div class="stat">
      <div class="stat-number">12</div>
      <div class="stat-label">Publications</div>
    </div>
    <div class="stat">
      <div class="stat-number">4</div>
      <div class="stat-label">Open-Source Tools</div>
    </div>
    <div class="stat">
      <div class="stat-number">7</div>
      <div class="stat-label">Industry Partners</div>
    </div>
    <div class="stat">
      <div class="stat-number">3</div>
      <div class="stat-label">Active Grants</div>
    </div>
  </div>
</section>

<section class="section">
  <div class="section-title">
    <h2>Selected Papers</h2>
    <a href="{{ '/papers/' | relative_url }}">View all</a>
  </div>
  <ul class="timeline">
    {% for pub in site.data.publications limit:2 %}
    <li>
      <strong>{{ pub.title }}</strong><br>
      {{ pub.authors }}<br>
      <span class="card-meta">{{ pub.venue }} ({{ pub.year }})</span>
    </li>
    {% endfor %}
  </ul>
</section>

<section class="section">
  <div class="section-title">
    <h2>Featured Projects</h2>
    <a href="{{ '/projects/' | relative_url }}">View all</a>
  </div>
  <div class="card-grid">
    {% for project in site.data.projects limit:2 %}
    <div class="card">
      <h3>{{ project.name }}</h3>
      <div class="card-meta">{{ project.role }}</div>
      <p>{{ project.description }}</p>
      <div class="tag-list">
        {% for tech in project.tech %}
        <span class="tag">{{ tech }}</span>
        {% endfor %}
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section-title">
    <h2>Recent Experience</h2>
    <a href="{{ '/experience/' | relative_url }}">View all</a>
  </div>
  <div class="card-grid">
    {% for role in site.data.experience limit:2 %}
    <div class="card">
      <h3>{{ role.role }}</h3>
      <div class="card-meta">{{ role.org }} | {{ role.start }} - {{ role.end }}</div>
      <p>{{ role.summary }}</p>
    </div>
    {% endfor %}
  </div>
</section>
