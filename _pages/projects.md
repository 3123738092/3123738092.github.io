---
layout: page
title: projects
permalink: /projects/
description: Selected research and course projects.
nav: true
nav_order: 3
display_categories: [research, project]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category | capitalize }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      <div class="col mb-4">
        <a href="{{ project.url | relative_url }}">
          <div class="card h-100 hoverable">
            {% if project.img %}
              <img
                src="{{ project.img | relative_url }}"
                class="card-img-top"
                alt="project thumbnail"
                style="height: 160px; object-fit: cover"
                loading="lazy"
              >
            {% endif %}
            <div class="card-body p-3">
              <h3 class="card-title" style="font-size: 1rem; font-weight: 600; margin-bottom: 0.4rem">{{ project.title }}</h3>
              <p class="card-text" style="font-size: 0.82rem; line-height: 1.45; margin-bottom: 0">{{ project.description }}</p>
            </div>
          </div>
        </a>
      </div>
    {% endfor %}
  </div>
{% endfor %}
</div>
