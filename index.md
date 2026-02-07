---
title: "Home"
layout: splash
permalink: /
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/hero.jpg
excerpt: >
  Helping people memorize, internalize, and live Scripture through disciplined practice.
---

## Welcome to the Proof of Concept

This Jekyll-powered space demonstrates how a Minimal Mistakes site can host essays, multimedia, coordinated events, and experimental workflows—all from the same repository. The sections below highlight real content types, curated calls to action, and a flexible layout that evolves with every new post, video, or product drop.

### What the site already shows

<div class="row">
  <article class="col-6">
    <h3>Editorial groundwork</h3>
    <p>Dummy blog posts track layout, tags, and category behavior so we can see how summaries, dates, and metadata render across different skins.</p>
  </article>
  <article class="col-6">
    <h3>Media &amp; events</h3>
    <p>Video walkthroughs, podcast notes, and event listings appear in their dedicated collections (`/videos/`, `/podcasts/`, `/events/`), proving the theme can surface varied content in one navigation.</p>
  </article>
</div>

<hr />

## Feature highlights

<div class="cards-grid">
  <article class="card">
    <header>
      <p class="card-meta">Layouts &amp; typography</p>
      <h3>Minimal Mistakes skins</h3>
    </header>
    <p>Switch `minimal_mistakes_skin` to test `air`, `default`, or `dark`. Each skin pairs with responsive type scales, featured cards, and hero behaviors that are already wired into this home layout.</p>
  </article>
  <article class="card">
    <header>
      <p class="card-meta">Collections</p>
      <h3>Posts, podcasts, and more</h3>
    </header>
    <p>Every collection in the repo—blog, videos, podcasts, store, and events—instantly generates archive pages. The grid below links to the main hubs for quick validation.</p>
  </article>
  <article class="card">
    <header>
      <p class="card-meta">Workflow demo</p>
      <h3>Updates ready for review</h3>
    </header>
    <p>Drop new markdown files into `_posts/`, `videos/`, or `_data/` and let the static build render previews. This page itself can grow with tabs, testimonials, or sponsor callouts as needed.</p>
  </article>
</div>

## Featured Collections

<div class="row">
  <div class="col-4">
    <h4>Blog</h4>
    <p>Chronological essays and testing notes.</p>
    <p><a href="{{ '/blog/' | relative_url }}">Visit the blog archive →</a></p>
  </div>
  <div class="col-4">
    <h4>Videos</h4>
    <p>Demos that prove the site can host multimedia while retaining minimal shell.</p>
    <p><a href="{{ '/videos/' | relative_url }}">Browse videos →</a></p>
  </div>
  <div class="col-4">
    <h4>Podcasts &amp; events</h4>
    <p>Audio and live sessions ready for presentation to donors or collaborators.</p>
    <p><a href="{{ '/podcasts/' | relative_url }}">Hear the podcasts →</a></p>
  </div>
</div>

## Latest drafts

<div class="post-grid">
  {% assign latest = site.posts | sort: "date" | reverse | slice: 0, 4 %}
  {% for post in latest %}
    <article class="card">
      <header>
        <p class="card-meta">{{ post.date | date: "%b %-d, %Y" }} • {{ post.categories | array_to_sentence_string }}</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      </header>
      <p>{{ post.summary }}</p>
    </article>
  {% endfor %}
</div>

## Ready for the next jump

Want to showcase more—like product cards, testimonials, or custom data-driven tables? Add shortcodes, leverage `includes`, or experiment with `data` files. Every new sample verifies that this Jekyll site remains flexible and future proof.
