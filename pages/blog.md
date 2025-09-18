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

<section class="bg-navy">
  <div class="container col-xxl-8 p-5">
    {% for post in site.posts %}
    <div class="card post-card mb-4">
      {%- if post.heroimage -%}
      <figure class="hero-image post mb-0">
        {% picture "{{ post.heroimage }}" --alt {{ post.heroimagealt }} %}
      </figure>  
      {%- endif -%}
      <div class="card-body text-light">
        <h2 class="mb-3">{{ post.title }}</h2>
        <p class="card-text mb-3 fs-6">{{ post.excerpt }}</p>
          {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <div class="card-text fs-6">
          {%- if post.author -%}{{ post.author }} •&nbsp;{%- endif -%}
          <time class="dt-published" datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: date_format }}</time>
        </div>
        <a href="{{ post.url }}" class="stretched-link" aria-label="continue reading"></a>
      </div>
    </div>
    {% endfor %}
  </div>
</section>
