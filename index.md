---
layout: default
title: Home
permalink: /
---

<div class="home">
  <h1 class="home-title">{{ site.title }}</h1>
  <p class="home-tagline">{{ site.tagline }}</p>

  <div class="home-categories">
    <a class="category-card" href="{{ '/spurs/' | relative_url }}">Spurs</a>
    <a class="category-card" href="{{ '/actors/' | relative_url }}">Actors</a>
    <a class="category-card" href="{{ '/memories/' | relative_url }}">Memories</a>
  </div>
</div>
