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
      <span class="category-icon">⚽</span>
      Spurs
    </a>
    <a class="category-card category-card--actors" href="{{ '/actors/' | relative_url }}">
      <span class="category-icon">🎬</span>
      Actors
    </a>
    <a class="category-card category-card--memories" href="{{ '/memories/' | relative_url }}">
      <span class="category-icon">📷</span>
      Memories
    </a>
  </div>
</div>
