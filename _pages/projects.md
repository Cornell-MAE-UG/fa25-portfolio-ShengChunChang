---
layout: default
title: Projects
permalink: /projects/
---
## Independent Projects
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
---
## Collaborative Projects (school required)
<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" />
          <p>{{ project.title}}</p>
        </a>
      </div>
    {% endfor %}
</div>
</div>

