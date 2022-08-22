---
layout: default
title: Resources
description: Thoughts and other resources from the PRX Tech Team
permalink: /blog
image: /assets/img/og-image.jpg
---
<header class="post-header bg-black-diagonal text-white lede hero px-5 pb-5 m-0">
  <div class="hero-content container col-xxl-8">
    <div class="hero-content-inner">
      <h1 class="display-5 post-title p-name" itemprop="name headline">Resources</h1>
      <p class="lead fs-4">Thoughts and other resources from the PRX Tech Team</p>
    </div>
  </div>
</header>

<section>
  <div class="container col-xxl-8 p-5">
    {% for post in site.posts %}
    <div class="row g-0 border bg-white rounded overflow-hidden flex-md-row mt-0 mb-4 shadow-sm h-md-250 position-relative">
      <div class="col p-4 d-flex flex-column position-static">
        <h2>{{ post.title }}</h2>
        <p class="card-text mb-4">{{ post.excerpt }}</p>
          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <div class="mb-1 text-muted">
          {%- if post.author -%}{{ post.author }} •&nbsp;{%- endif -%}
          <time class="dt-published" datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: date_format }}</time>
        </div>
        <a href="{{ post.url }}" class="stretched-link" aria-label="continue reading"></a>
      </div>
      {%- if post.heroimage -%}
      <div class="col-3 p-4 thumbnail d-none d-lg-block blog-thumbnail">
        {% picture thumbnail "{{ post.heroimage }}" --alt {{ post.heroimagealt }} %}
      </div>
      {%- endif -%}
    </div>
    {% endfor %}
  </div>
</section>
