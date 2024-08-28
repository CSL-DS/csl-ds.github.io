---
layout: team
title: Team
permalink: /team/
background: https://images.unsplash.com/photo-1562577308-c8b2614b9b9a?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

<div class="team-grid">
  {% for member in site._data.team.yml %}
    {% if member.section %}
      <div class="section-divider">
        <h2>{{ member.section }}</h2>
        <p>{{ member.description }}</p>
      </div>
    {% else %}
      <div class="team-member">
        <img src="{{ member.image | relative_url }}" alt="{{ member.name }}">
        <h3>{{ member.name }}</h3>
        <p class="role">{{ member.role }}</p>
        <div class="description">
          {{ member.description | markdownify }}
        </div>
        <div class="social-links">
          {% if member.email %}
            <a href="mailto:{{ member.email }}" title="Email"><i class="fas fa-envelope"></i></a>
          {% endif %}
          {% if member.github %}
            <a href="https://github.com/{{ member.github }}" title="GitHub"><i class="fab fa-github"></i></a>
          {% endif %}
          {% if member.twitter %}
            <a href="https://twitter.com/{{ member.twitter }}" title="Twitter"><i class="fab fa-twitter"></i></a>
          {% endif %}
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>

<style>
  .team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
  }
  .team-member {
    border: 1px solid #ddd;
    padding: 1rem;
    text-align: center;
  }
  .team-member img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50%;
  }
  .social-links {
    margin-top: 1rem;
  }
  .social-links a {
    margin: 0 0.5rem;
    font-size: 1.2rem;
  }
  .section-divider {
    grid-column: 1 / -1;
    text-align: center;
    margin: 2rem 0;
    padding: 1rem;
    background-color: #f0f0f0;
    border-radius: 8px;
  }
  .section-divider h2 {
    font-size: 1.8rem;
    margin-bottom: 0.5rem;
  }
  .section-divider p {
    font-size: 1.1rem;
  }
  .description p {
    margin: 0;
  }
</style>
