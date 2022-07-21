---
layout: default
permalink: /blog
---
<header class="post-header bg-black-diagonal text-white lede hero px-4 pb-4 m-0">
  <div class="hero-content container col-xxl-8">
    <div class="hero-content-inner">
      <h1 class="display-5 post-title p-name" itemprop="name headline">Blog</h1>
      <p class="lead fs-3">Posts from the PRX Tech Team</p>
    </div>
  </div>
</header>

<section>
  <div class="container col-xxl-8 p-4">
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    {% for post in site.posts %}
    <div class="row g-0 border bg-white rounded overflow-hidden flex-md-row mt-0 mb-4 shadow-sm h-md-250 position-relative">
      <div class="col p-4 d-flex flex-column position-static">
        <h3>{{ post.title }}</h3>
        <p class="card-text mb-4">{{ post.excerpt }}</p>
        <div class="mb-1 text-muted">{{ post.date }}</div>
        <a href="{{ post.url }}" class="stretched-link visually-hidden">Continue reading</a>
      </div>
      {%- if post.heroimage -%}
      <div class="col-3 p-4 thumbnail d-none d-lg-block">
        {% picture thumbnail "{{ post.heroimage }}" --alt {{ post.heroimagealt }} %}
      </div>
      {%- endif -%}
    </div>
    {% endfor %}
  </div>
</section>
