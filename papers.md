---
layout: page
title: Papers
subtitle: "Peer-reviewed publications, preprints, and selected talks."
permalink: /papers/
---

<ul class="timeline">
  {% for pub in site.data.publications %}
  <li>
    <strong>{{ pub.title }}</strong><br>
    {{ pub.authors }}<br>
    <span class="card-meta">{{ pub.venue }} ({{ pub.year }})</span>
    <div class="tag-list">
      {% if pub.links.pdf %}<a class="tag" href="{{ pub.links.pdf }}">PDF</a>{% endif %}
      {% if pub.links.code %}<a class="tag" href="{{ pub.links.code }}">Code</a>{% endif %}
      {% if pub.links.doi %}<a class="tag" href="{{ pub.links.doi }}">DOI</a>{% endif %}
      {% if pub.links.project %}<a class="tag" href="{{ pub.links.project }}">Project</a>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
