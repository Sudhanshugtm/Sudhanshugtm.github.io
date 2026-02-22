---
layout: default
title: Writing
description: Essays, notes, and links.
---

<div class="writing-simple">
  <h1>Writing</h1>

  <ul class="post-list-simple">
    {% for post in site.posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
  </ul>
</div>
