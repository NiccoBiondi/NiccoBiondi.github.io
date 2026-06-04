---
layout: page
title: projects
permalink: /projects/
description: Research projects and project pages.
nav: true
nav_order: 3
---

<div class="post">
  <ul class="project-list" style="list-style: none; padding: 0;">
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
    <li style="margin-bottom: 2rem;">
      <div class="row align-items-center">
        {% if project.img %}
        <div class="col-sm-3" style="margin-bottom: 0.5rem;">
          <a href="{{ project.url | relative_url }}">
            <img src="{{ project.img | relative_url }}" alt="{{ project.title }}" class="img-fluid rounded" style="object-fit: cover; max-height: 120px; width: 100%;">
          </a>
        </div>
        <div class="col-sm-9">
        {% else %}
        <div class="col-12">
        {% endif %}
          <h3 style="margin-bottom: 0.25rem;">
            <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
          </h3>
          {% if project.description %}
          <p style="margin-bottom: 0; color: var(--global-text-color-light);">{{ project.description }}</p>
          {% endif %}
        </div>
      </div>
    </li>
    {% endfor %}
  </ul>
</div>
