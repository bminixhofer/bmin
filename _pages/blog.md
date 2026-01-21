---
layout: page
title: bminlog
permalink: /blog/
---

<h1>b<span style="color: var(--global-theme-color);">min</span>log</h1>

{% for post in site.posts %}
  <div class="post-item">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% endif %}
  </div>
  <hr>
{% endfor %}

{% if site.posts.size == 0 %}
  <p>No blog posts yet.</p>
{% endif %}