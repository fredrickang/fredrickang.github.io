---
layout: page
permalink: /repositories/
title: repositories
description: Open-source artifacts for research in real-time systems and multi-DNN inference.
nav: true
nav_order: 4
---

## Research repositories

<div class="row row-cols-1 row-cols-md-2 repository-grid">
  {% for repo in site.data.repositories.github_repos %}
    <div class="col mb-4">
      <a class="repository-card-link" href="{{ repo.url }}" target="_blank" rel="external nofollow noopener">
        <article class="card repository-card h-100 hoverable">
          <div class="card-body d-flex flex-column">
            <div class="repository-card-heading">
              <i class="fa-brands fa-github" aria-hidden="true"></i>
              <h2 class="card-title">{{ repo.name }}</h2>
            </div>
            <p class="repository-path">{{ repo.repository }}</p>
            <p class="card-text">{{ repo.description }}</p>
            <div class="repository-meta mt-auto">
              <span>{{ repo.language }}</span>
              <span>{{ repo.venue }}</span>
            </div>
          </div>
        </article>
      </a>
    </div>
  {% endfor %}
</div>
