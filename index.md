---
layout: default
title: Home
---

<div class="recipe-grid">
{% assign sorted = site.recipes | sort: "title" %}
{% for recipe in sorted %}
  <a href="{{ recipe.url | relative_url }}" class="recipe-card">
    <h2>{{ recipe.title }}</h2>
    <span class="category">{{ recipe.category }}</span>
  </a>
{% endfor %}
</div>
