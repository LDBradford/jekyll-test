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

<div class="card-grid">
  <article class="card">
    <header>
      <p class="card-meta">Editorial groundwork</p>
      <h3>Blog experiments</h3>
    </header>
    <p>Dummy posts record layout, metadata, and category behavior so we can validate the workflow for summaries and featured cards.</p>
  </article>
  <article class="card">
    <header>
      <p class="card-meta">Media &amp; events</p>
      <h3>Collections in action</h3>
    </header>
    <p>Podcasts, videos, store items, and events live under their own collections, demonstrating that Minimal Mistakes can surface mixed content from a single repo.</p>
  </article>
</div>

<hr />

## Feature highlights

<div class="card-grid">
  <article class="card">
    <header>
      <p class="card-meta">Layouts &amp; typography</p>
      <h3>Minimal Mistakes skins</h3>
    </header>
    <p>Switch `minimal_mistakes_skin` to test `air`, `default`, or `dark`. Each skin applies responsive type scales, featured cards, and hero styles that adapt to your content automatically.</p>
  </article>
  <article class="card">
    <header>
      <p class="card-meta">Collections</p>
      <h3>Posts, podcasts, and more</h3>
    </header>
    <p>Every collection—blog, videos, podcasts, events, store—instantly generates archives. Keep adding markdown and note how the theme keeps navigation and cards consistent.</p>
  </article>
  <article class="card">
    <header>
      <p class="card-meta">Workflow demo</p>
      <h3>Updates ready for review</h3>
    </header>
    <p>Drop new markdown into `_posts/`, `/videos`, or `_data/navigation.yml` and the build renders previews immediately. This landing page can grow with tabs, testimonials, and sponsor callouts too.</p>
  </article>
</div>

## Featured collections

<div class="card-grid">
  <article class="card">
    <header>
      <h4>Blog</h4>
    </header>
    <p>Chronological essays and testing notes.</p>
    <p><a href="{{ '/blog/' | relative_url }}">Visit the blog archive →</a></p>
  </article>
  <article class="card">
    <header>
      <h4>Videos</h4>
    </header>
    <p>Demos that prove multimedia assets play nicely while the shell stays minimal.</p>
    <p><a href="{{ '/videos/' | relative_url }}">Browse videos →</a></p>
  </article>
  <article class="card">
    <header>
      <h4>Podcasts &amp; events</h4>
    </header>
    <p>Audio notes and live sessions ready for sponsors or collaborators.</p>
    <p><a href="{{ '/podcasts/' | relative_url }}">Hear the podcasts →</a></p>
  </article>
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
