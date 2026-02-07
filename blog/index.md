---
layout: single
title: "Blog"
permalink: /blog/
author_profile: false
---

## Proof of Concept Journal

This space collects reflective entries, lightweight experiments, and coordination notes that help us vet the Minimal Mistakes setup before we ship anything more polished. Everything below is intentionally structured so we can test layout, navigation, search, and filtering without cluttering the production feed.

### Quick Actions

<div class="blog-actions">
  <form class="search-form" action="{{ '/search/' | relative_url }}" method="get">
    <label class="sr-only" for="blog-search">Search the blog</label>
    <input id="blog-search" name="q" type="search" placeholder="Search topics—typography, automation, design..." />
    <button type="submit">Search</button>
  </form>
  <div class="filters">
    <button class="filter-pill" type="button">Recent</button>
    <button class="filter-pill" type="button">Testing</button>
    <button class="filter-pill" type="button">Process</button>
    <button class="filter-pill" type="button">Community</button>
  </div>
</div>

### Filtered Views

<div class="filter-spotlight">
  <article>
    <h3>Category spotlight: Testing</h3>
    <p>Oriented around the `testing` category to see how the archive handles a dense collection of experiments.</p>
    <ul>
      {% assign testing_posts = site.categories.testing | sort: "date" | reverse %}
      {% for post in testing_posts %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%b %-d, %Y" }}
        </li>
      {% endfor %}
    </ul>
  </article>
  <article>
    <h3>Tag spotlight: design</h3>
    <p>Use this list to watch the tag-driven filters gracefully degrade when there are fewer entries.</p>
    <ul>
      {% assign design_tag = site.tags.design %}
      {% for post in design_tag %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a> — {{ post.summary }}
        </li>
      {% endfor %}
    </ul>
  </article>
</div>

### Recent posts

<div class="post-grid">
  {% assign recent_posts = site.posts | sort: "date" | reverse | slice: 0, 6 %}
  {% for post in recent_posts %}
    <article class="card">
      <header>
        <p class="card-meta">
          {{ post.date | date: "%b %-d, %Y" }} • {{ post.categories | array_to_sentence_string }}
        </p>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      </header>
      <p>{{ post.summary }}</p>
      <p class="card-tags">
        {% for tag in post.tags %}
          <span class="tag">{{ tag }}</span>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      </p>
    </article>
  {% endfor %}
</div>

### Need more?

If you would like to push the experience further, try swapping in a different Minimal Mistakes skin, enabling search via Algolia, or introducing a curated callout area for featured posts. Keep iterating until every interaction on this page is supported and test-ready.
