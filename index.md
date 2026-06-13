---
layout: default
title: Home
permalink: /
---

<div class="home">
  <h1 class="home-title">{{ site.title }}</h1>
  <p class="home-tagline">{{ site.tagline }}</p>

  <div class="home-categories">
    <a class="category-card category-card--spurs" href="{{ '/spurs/' | relative_url }}">
      {% if site.data.icons.spurs and site.data.icons.spurs != "" %}
        <img class="category-icon category-icon--img" src="{{ site.data.icons.spurs | relative_url }}" alt="">
      {% else %}
        <span class="category-icon">⚽</span>
      {% endif %}
      Spurs
    </a>
    <a class="category-card category-card--lovers" href="{{ '/lovers/' | relative_url }}">
      {% if site.data.icons.lovers and site.data.icons.lovers != "" %}
        <img class="category-icon category-icon--img" src="{{ site.data.icons.lovers | relative_url }}" alt="">
      {% else %}
        <span class="category-icon">💜</span>
      {% endif %}
      Lovers
    </a>
    <a class="category-card category-card--memories" href="{{ '/memories/' | relative_url }}">
      {% if site.data.icons.memories and site.data.icons.memories != "" %}
        <img class="category-icon category-icon--img" src="{{ site.data.icons.memories | relative_url }}" alt="">
      {% else %}
        <span class="category-icon">📷</span>
      {% endif %}
      Memories
    </a>
  </div>
</div>
