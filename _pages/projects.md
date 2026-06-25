---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-header">
  <p class="section-label">// Project Archive</p>
  <h2>Independent Projects</h2>
</div>

<div class="gallery-container">
  <div class="project-gallery">
    {% for indproject in site.indprojects %}
      <div class="gallery-item">
        <a href="{{ indproject.url | relative_url }}">
          <img src="{{ indproject.image | relative_url }}" alt="{{ indproject.title }}" />
          <p>{{ indproject.title }}</p>
        </a>
      </div>
    {% endfor %}
  </div>
</div>

{% if site.show_school_projects %}
<hr class="section-divider">

<div class="projects-header">
  <p class="section-label">// Collaborative Missions</p>
  <h2>School Projects</h2>
</div>

<div class="gallery-container">
  <div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p>{{ project.title }}</p>
        </a>
      </div>
    {% endfor %}
  </div>
</div>
{% endif %}
