---
layout: default
title: Home
permalink: /
---

<div class="home">
  <h1 class="home-title">{{ site.title }}</h1>
  <p class="home-tagline">{{ site.tagline }}</p>

  {% if site.data.home.banner and site.data.home.banner != "" %}
    <div class="home-banner">
      <img src="{{ site.data.home.banner | relative_url }}" alt="">
    </div>
  {% else %}
    <div class="home-banner home-banner--empty">
      <span>이미지를 업로드해주세요</span>
    </div>
  {% endif %}

  <h2 class="home-section-title">Rincones de CasA</h2>

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

  <h2 class="home-section-title home-section-title--recent">Recent Posts</h2>

  {% assign recent_posts = site.posts | slice: 0, 5 %}
  {% if recent_posts.size > 0 %}
    <ul class="recent-post-list">
      {% for post in recent_posts %}
        {% assign cat = post.categories | first %}
        <li>
          <span class="recent-post-category recent-post-category--{{ cat }}">{{ cat | capitalize }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p class="empty">아직 작성된 글이 없습니다.</p>
  {% endif %}
</div>
