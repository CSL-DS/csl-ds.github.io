---
layout: team
title: Team
permalink: /team/
background: https://images.unsplash.com/photo-1562577308-c8b2614b9b9a?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---
{% for member in site._data.team.yml %}
  {% if member.section %}
    <div class="section-divider">
      <h2>{{ member.section }}</h2>
      {% if member.description %}
        <p>{{ member.description }}</p>
      {% endif %}
    </div>
  {% else %}
    <div class="team-member">
      <!-- 기존의 팀 멤버 표시 코드 -->
    </div>
  {% endif %}
{% endfor %}

<style>
  .section-divider {
    margin: 2rem 0;
  }
  .section-divider h2 {
    font-size: 2rem;
    margin-bottom: 0.5rem;
    border: none;
  }
  .section-divider p {
    font-size: 1.1rem;
  }
</style>
