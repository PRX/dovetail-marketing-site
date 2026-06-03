---
layout: page
title: "Coming soon: The Dovetail Ad Marketplace"
description: A new self-service marketplace for stations to generate revenue from unsold inventory in a brand-safe way, and for advertisers to reach Public Media audiences at scale.
permalink: /ad-marketplace
image: /assets/img/og-image.jpg
---
<section class="text-white lede hero px-5 pb-5 m-0">
  <div class="hero-image">
    <div>
    {% picture img/dt-hero-marketplace.jpg --alt Split-screen interface showing a data dashboard with inventory metrics and a blue overlay. Graphs and a recent save indicator are visible, conveying a tech-focused, analytical tone. %}
    </div>
  </div>
  <div class="hero-content container col-xxl-8">
    <div class="row">
      <div class="col-md-8">
        <div class="hero-content-inner">
          <h1 class="mb-4 fw-bold">Coming soon: The Dovetail Ad Marketplace</h1>
          <p>A new self-service podcasting ad marketplace for stations to generate revenue from unsold inventory in a brand-safe way, and for advertisers to reach Public Media audiences at scale with efficiency.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="section bg-navy text-white p-5">
  <div class="container col-xxl-8">
    <h2 class="mb-3">For Public Media Stations</h2>
    <p>PRX is expanding Dovetail by creating a self-service ad marketplace. It will allow advertisers to purchase public media podcast ad inventory directly by accessing inventory that isn’t being used by direct sales, all without requiring manual intervention from your team.</p>
    <ul>
      <li>Gain new revenue from unsold inventory.</li>
      <li>No minimum downloads required to be included in the network.</li>
      <li>Join the national <em>Public Media Station Channel</em> AND create station specific bundles.</li>
      <li>Revenue shares for your team’s sales into the Ad Marketplace.</li>
      <li>Brand Safety you can trust, all advertisers are approved by PRX.</li>
      <li>No extra work, sign up and watch revenue flow in.</li>
      <li>Another avenue to grow your podcast audience through buying cross-promotions across the national channel.</li>
    </ul>
  </div>
</section>

<section class="section bg-gray-x p-5">
  <div class="container col-xxl-8">
    <h2 class="mb-3">For Advertisers</h2>
    <p>The Dovetail Ad Marketplace is the self-service way for reaching Public Media audiences. Think of it as a direct line to premium public media audiences without the complexity of programmatic buying.</p>
    <ul>
      <li><strong>Brand-safe environment</strong>: You’re buying into curated, premium content, not open auction inventory.</li>
      <li><strong>Simple, transparent pricing</strong>: You know what you’ll pay before you buy.</li>
      <li><strong>Self-service speed</strong>: Agree to terms, bring your own creative, place a buy, and your ad will be running with only one quick approval.</li>
      <li><strong>Audience reach by channel</strong>: Channels group shows by theme, station, or geography, so you can reach the right mix of listeners without needing to research individual podcasts.</li>
      <li><strong>Built in reporting</strong>: for confidence in your ad spend.</li>
    </ul>
  </div>
</section>

<div class="p-5 bg-navy text-white">
  <div class="container col-xxl-8">
    <div class="post-content">
      <h2 class="display-6">Let us know if you are interested</h2>
      <p>If you are a Station or Advertiser interested in participating in the Dovetail Ad Marketplace, please fill out this form and we will start a discussion on best meeting your needs.</p>
      {% if jekyll.environment == 'production' -%}
      <form name="marketplace_interest_form" accept-charset="UTF-8" action="https://g26e6h83r5.execute-api.us-east-1.amazonaws.com/v1/submit" method="POST">
      {%- else -%}
      <form name="marketplace_interest_form" accept-charset="UTF-8" action="https://dsmt2m9oj5.execute-api.us-east-1.amazonaws.com/v1/submit" method="POST">
      {%- endif %}
        <div class="form-group">
          <label for="inputName">Name*</label>
          <input type="text" class="form-control" id="inputName" name="inputName" aria-describedby="inputName" placeholder="Enter your name" required>
        </div>
        <div class="form-group">
          <label for="inputEmail">Email address*</label>
          <input type="email" class="form-control" id="inputEmail" name="inputEmail" aria-describedby="emailHelp" placeholder="Enter email" required>
          <small class="form-text">We'll never share your email with anyone else.</small>
        </div>
        <div class="form-group">
          <label for="textOrganization">Organization Name</label>
          <input type="text" class="form-control" id="textOrganization" name="textOrganization" aria-describedby="textOrganization" placeholder="Enter your organization">
        </div>
        <div class="form-group">
          <label for="selectOrgType">Which best describes your Organization?</label>
          <select name="orgType" id="selectOrgType" class="form-control form-select">
            <option value="">--Please choose an option--</option>
            <option value="ad-agency">Ad Agency</option>
            <option value="advertiser">Advertiser</option>
            <option value="podcast-producer">Podcast Producer</option>
            <option value="public-media-station">Public Media Station</option>
          </select>
        </div>
        <div class="form-group">
          <label for="textJobTitle">Job Title</label>
          <input type="text" class="form-control" id="textJobTitle" name="textJobTitle" aria-describedby="textJobTitle" placeholder="Enter your job title">
        </div>
        <div class="form-group">
          <label for="textPhone">Phone Number</label>
          <input type="text" class="form-control" id="textPhone" name="textPhone" aria-describedby="textPhone" placeholder="(xxx)-xxx-xxxx">
        </div>
        <div class="cf-turnstile" data-sitekey="#"></div>
        <input type="hidden" id="messageType" name="messageType" value="marketplace" />
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
  </div>
</div>
