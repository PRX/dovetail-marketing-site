---
layout: default
permalink: /
image: /assets/img/og-image.jpg
---

<section class="section top text-white">
  {% include components/show-tiles.html %}
  <div class="container col-xxl-9 position-relative p-4">
    <h1 class="mb-4 mt-4">The podcast publishing and monetization platform for professionals</h1>
    <p class="mb-6 pe-4 fs-6">Dovetail from PRX is the all-in-one platform trusted by podcasting professionals. We help you expand your audience, monetize content, and ensure long-term sustainability—all while maintaining a steadfast commitment to privacy. From independent creators to industry leaders, Dovetail scales with you, supporting your podcast's journey every step of the way.</p>
    <a href="{% link pages/contact.md %}" type="button" class="btn btn-primary px-4 mt-2"><nobr>Let's Talk</nobr></a>
    </div>
  </div>
</section>

<div class="section bg-navy m-0 p-0 text-white">
  <div class="container">
    {% include components/brand-logos.html %}
  </div>
</div>

<div class="home-sections">
  {% for section in site.data.section_home %}
    {%- include section-home.html
      image=section.image
      image-alt=section.image-alt
      title=section.title
      tagline=section.tagline
      features=section.features
    -%}
  {% endfor %}
</div>

<section class="section bg-navy section-quote text-white p-4 prx-70vh">
  <div class="container-fluid">
    <h2 class="display-6 mb-4 text-center">Don't just take our word for it</h2>
    <div class="row g-5">
      <figure class="col-md-5 mb-0 px-4">
        <blockquote class="blockquote mt-2">
          <p>“Dovetail has turned out to be more than just a tool for us. Because of the way that you've supported us in the transition, it's helped us strengthen our creator community. We have in-house podcasts, but we also work with teams that operate mostly independently. We're able to offer them so much more now, which has allowed us to expand our podcast network into something more robust. Having a tool that truly meets our needs is the glue.”</p>
        </blockquote>
        <figcaption class="blockquote-footer fs-6">
          Shereen Adel, KALW
        </figcaption>
      </figure>

      <figure class="col-md-5 mb-0 px-4">
        <blockquote class="blockquote mt-2">
          <p>“Dovetail has really allowed us to streamline podcast operations — from production to marketing support and data-driven decision making. PRX’s tools integrate well with other tools across the industry, which has allowed us to build a single process that works well for us where we are right now. And there’s a lot of room to grow!”</p>
        </blockquote>
        <figcaption class="blockquote-footer fs-6">
          Whitney Baker, WUNC
        </figcaption>
      </figure>

      <div class="quote-mark icon-svg d-flex justify-content-center col-2">
        <img src="/assets/img/quote.svg" alt="quotation mark" aria-hidden="true" class="" width="100" height="79" />
      </div>
    </div>
  </div>
</section>

<section class="section hero p-5">
  <div class="hero-image">
    <div>
    {% picture img/hero-privacy.jpg --alt Headphones on an orange background %}
    </div>
  </div>
  <div class="hero-content container col-xxl-8">
    <div class="row">
      <div class="col-md-8">
        <div class="hero-content-inner">
          <h2 class="display-6 mb-4">Built with listener privacy in mind</h2>
          <p class="fs-5">PRX is taking the lead in establishing standards that ensure the safety of audiences while maximizing revenue opportunities.</p>
          <p class="fs-5"><strong>Why should you care about privacy?</strong></p>
          <div class="row g-4">
            <div class="col d-flex align-items-start">
              <div>
                <ul>
                  <li><strong>Mission:</strong> Trust is a two-way street. Public media's ability to thrive depends on the trust our listeners place in us.  Using personal data without permission violates that trust.</li>
                  <li><strong>Compliance:</strong> Privacy regulations are strengthening, not weakening.  It is essential for content creators to be ready.</li>
                  <li><strong>Technology:</strong>  Big tech companies like Apple are taking a stand on privacy and will force others to do the same. PRX is an active leader in building values-based technology on behalf of all of our partners.</li>
                </ul>
              </div>
            </div>
          </div>
          <p class="mb-4"><a href="{% link pages/contact.md %}" type="button" class="btn btn-primary px-4 gap-3">Let's Talk</a></p>
        </div>
      </div>
    </div>
  </div>
</section>

<aside class="section text-white hero p-5 m-0 cta">
  <div class="hero-image">
    <div>{% picture img/cta-hero.jpg --alt Open laptop with a podcasting microphone in foreground %}</div>
  </div>
  <div class="hero-content container col-xxl-8 text-center py-4">
    <div class="hero-content-inner">
      <h2 class="display-6 pt-4">Ensure your podcast keeps its independence</h2>
      <p class="fs-3 mt-2 mb-4">Reach out today</p>
      <p class="text-center"><a href="{% link pages/contact.md %}" type="button" class="btn btn-primary px-4 gap-3">Let's Talk</a></p>
    </div>
  </div>
</aside>
