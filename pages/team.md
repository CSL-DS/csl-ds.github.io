---
layout: team
title: Team
permalink: /team/
background: https://images.unsplash.com/photo-1562577308-c8b2614b9b9a?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---
{% assign categories = site.data.team | group_by: "category" %}

{% for category in categories %}
  <h2>{{ category.name }}</h2>
  <div class="row">
    {% for member in category.items %}
      <div class="col-lg-4 col-sm-6">
        <div class="team-member">
          <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" class="img-fluid rounded-circle">
          <h4>{{ member.name }}</h4>
          <p class="text-muted">{{ member.role }}</p>
          {{ member.description | markdownify }}
          <ul class="list-inline social-buttons">
            {% if member.email %}
              <li class="list-inline-item">
                <a href="mailto:{{ member.email }}">
                  <i class="fas fa-envelope"></i>
                </a>
              </li>
            {% endif %}
            {% if member.twitter %}
              <li class="list-inline-item">
                <a href="https://twitter.com/{{ member.twitter }}">
                  <i class="fab fa-twitter"></i>
                </a>
              </li>
            {% endif %}
            {% if member.github %}
              <li class="list-inline-item">
                <a href="https://github.com/{{ member.github }}">
                  <i class="fab fa-github"></i>
                </a>
              </li>
            {% endif %}
          </ul>
        </div>
      </div>
    {% endfor %}
  </div>
{% endfor %}
