---
layout: default
title: 首页
---

<div class="section-title">
  <span>最新文章 & 随想</span>
  <span class="post-count">共 {{ site.posts.size }} 篇</span>
</div>

<div class="post-grid">
  {% for post in site.posts %}
    <article class="post-card">
      <div class="post-card-header">
        <h2 class="post-card-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <span class="post-card-date">{{ post.date | date: "%Y-%m-%d" }}</span>
      </div>
      <div class="post-card-excerpt">
        {{ post.excerpt | strip_html | truncate: 120 }}
      </div>
      <div class="post-card-meta">
        {% if post.categories.size > 0 %}
          {% for cat in post.categories %}
            <span class="badge">📁 {{ cat }}</span>
          {% endfor %}
        {% endif %}
        {% if post.tags.size > 0 %}
          {% for tag in post.tags %}
            <span class="badge">🏷️ {{ tag }}</span>
          {% endfor %}
        {% endif %}
      </div>
    </article>
  {% endfor %}
</div>
