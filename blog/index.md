---
layout: single
title: "Blog"
permalink: /blog/
author_profile: false
---

## Proof of Concept Journal

A simple chronological list of placeholder posts so we can preview how the Minimal Mistakes blog layout behaves with real content.

<ul class="post-list">
  {% assign recent_posts = site.posts | sort: "date" | reverse %}
  {% for post in recent_posts %}
    <li class="post-list-item">
      <article>
        <header>
          <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }} • {{ post.categories | array_to_sentence_string }}</p>
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        </header>
        {% if post.summary %}
          <p>{{ post.summary }}</p>
        {% endif %}
      </article>
    </li>
  {% endfor %}
</ul>
