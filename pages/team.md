---
layout: default
title: Team
permalink: /team/
background: https://images.unsplash.com/photo-1562577308-c8b2614b9b9a?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

{% for member in site.data.team %}
  {% if member.name == "" %}
    <h2>{{ member.category }}</h2>
  {% else %}
    <div class="d-flex team-member">
      <div class="flex-shrink-0 me-3">
        {% if member.image %}
          <img src="{{ member.image | relative_url }}" alt="{{ member.name }}">
        {% endif %}
      </div>
      <div>
        <h5 id="{{ member.name | strip | url_encode }}">
          {{ member.name }}
          {% if member.role %}
            <small class="text-muted">| {{ member.role }}</small>
          {% endif %}
        </h5>
        {{ member.description | markdownify }}
        <ul class="list-inline">
          {% if member.orcid %}
            <li class="list-inline-item">
              <a href="https://orcid.org/{{ member.orcid }}"><i class="ai ai-orcid"></i></a>
            </li>
          {% endif %}
          {% if member.researchgate %}
            <li class="list-inline-item">
              <a href="https://researchgate.net/profile/{{ member.researchgate }}"><i class="ai ai-researchgate"></i></a>
            </li>
          {% endif %}
          {% if member.googlescholar %}
            <li class="list-inline-item">
              <a href="https://scholar.google.com/citations?user={{ member.googlescholar }}"><i class="ai ai-google-scholar"></i></a>
            </li>
          {% endif %}
          {% if member.twitter %}
            <li class="list-inline-item">
              <a href="https://twitter.com/{{ member.twitter }}"><i class="fab fa-twitter"></i></a>
            </li>
          {% endif %}
          {% if member.mastodon %}
            <li class="list-inline-item">
              <a href="{{ member.mastodon }}"><i class="fab fa-mastodon"></i></a>
            </li>
          {% endif %}
          {% if member.github %}
            <li class="list-inline-item">
              <a href="https://github.com/{{ member.github }}"><i class="fab fa-github"></i></a>
            </li>
          {% endif %}
          {% if member.email %}
            <li class="list-inline-item">
              <a href="mailto:{{ member.email }}"><i class="far fa-envelope"></i></a>
            </li>
          {% endif %}
        </ul>
      </div>
    </div>
  {% endif %}
{% endfor %}
