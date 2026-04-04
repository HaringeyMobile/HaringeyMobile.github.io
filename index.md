---
layout: page
title: Haringey Mobile
description: Educational and strategy games
---

## Our Apps

<div class="apps-grid">
{% for app in site.data.apps %}
  <article class="app-card">
    <div class="app-header">
      <img src="{{ app.icon | relative_url }}" alt="{{ app.name }} icon" />
      <h3 class="app-title">{{ app.name }}</h3>
      <p class="app-description">{{ app.description }}</p>
    </div>
    
    <div class="app-links">
      <a href="{{ app.play_store }}" target="_blank" rel="noopener">Get on Google Play</a>
      <a href="{{ app.license | relative_url }}">Privacy Policy</a>
      <a href="{{ app.terms | relative_url }}">Terms of Service</a>
      {% if app.deletion %}
        <a href="{{ app.deletion | relative_url }}">
          {% if app.suite == "Math Practice" %}
            Delete Math Practice Account
          {% else %}
            Delete Account
          {% endif %}
        </a>
      {% endif %}
    </div>
  </article>
{% endfor %}
</div>
