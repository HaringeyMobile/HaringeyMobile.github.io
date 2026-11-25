---
layout: page
title: Haringey Mobile
description: Educational and strategy games
---

## Our Apps

<div class="apps-grid">
{% for app in site.data.apps %}
{% if app.category == "main" %}
  <article class="app-card">
    <div class="app-header">
      <img src="{{ app.icon | relative_url }}" alt="{{ app.name }} icon" />
      <h3 class="app-title">{{ app.name }}</h3>
      <p class="app-description">{{ app.description }}</p>
    </div>

    <div class="app-links">
      <a href="{{ app.play_store }}" target="_blank" rel="noopener">Get on Google Play</a>
      {% if app.fdroid %}<a href="{{ app.fdroid }}" target="_blank" rel="noopener">Get on F-Droid</a>{% endif %}
      {% if app.source %}<a href="{{ app.source }}" target="_blank" rel="noopener">Source Code</a>{% endif %}
      {% if app.license %}<a href="{{ app.license }}"{% if app.license contains 'github.com' %} target="_blank" rel="noopener"{% endif %}>Privacy Policy</a>{% endif %}
      {% if app.terms %}<a href="{{ app.terms | relative_url }}">Terms of Service</a>{% endif %}
      {% if app.deletion %}<a href="{{ app.deletion | relative_url }}">Delete Account</a>{% endif %}
    </div>
  </article>
{% endif %}
{% endfor %}
</div>

<details class="legacy-apps">
  <summary>Legacy Apps</summary>
  <p>These standalone math apps have been consolidated into the new all-in-one <strong>Math Practice</strong> app. Their legal documents remain available here for existing users.</p>
  <div class="apps-grid">
  {% for app in site.data.apps %}
  {% if app.category == "legacy" %}
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
        <a href="{{ app.deletion | relative_url }}">Delete Account</a>
      </div>
    </article>
  {% endif %}
  {% endfor %}
  </div>
</details>
