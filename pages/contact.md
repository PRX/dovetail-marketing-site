---
layout: page
title: Contact
description: We want to know how we can help you with your podcasting needs.
permalink: /contact/
image: /assets/img/og-image.jpg
---
<header class="post-header bg-black-diagonal text-white lede hero px-5 pb-5 m-0">
  <div class="hero-content container col-xxl-8">
    <div class="hero-content-inner">
      <h1 class="display-5 post-title p-name" itemprop="name headline">Contact</h1>
      <p class="lead fs-4">We want to know how we can help you with your podcasting needs. We know forms are boring, but this will help us better understand your podcasting needs.</p>
    </div>
  </div>
</header>

<div class="p-5 bg-gray-x">
  <div class="container col-xxl-8">

  <div class="post-content">
    <h2 class="display-6">Tell us a little about yourself...</h2>
    <form name="contact_form" accept-charset="UTF-8" action="https://dsmt2m9oj5.execute-api.us-east-1.amazonaws.com/v1/submit" method="POST">
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
        <label for="textOrganization">Organization</label>
        <input type="text" class="form-control" id="textOrganization" name="textOrganization" aria-describedby="textOrganization" placeholder="Enter your organization">
      </div>
      <div class="form-group">
        <label for="textJobTitle">Job Title</label>
        <input type="text" class="form-control" id="textJobTitle" name="textJobTitle" aria-describedby="textJobTitle" placeholder="Enter your job title">
      </div>
      <div class="form-group">
        <label for="textPhone">Phone Number</label>
        <input type="text" class="form-control" id="textPhone" name="textPhone" aria-describedby="textPhone" placeholder="(xxx)-xxx-xxxx">
      </div>
      <hr />
      <h2 class="display-6">Tell us about your podcasts...</h2>
      <div class="form-group">
        <label for="numberPodcasts">How many podcasts do you currently have?</label>
        <input type="text" class="form-control" id="numberPodcasts" aria-describedby="numberPodcasts" name="numberPodcasts" placeholder="Enter number of podcasts">
      </div>
      <div class="form-group">
        <label for="inputAvgDownloads">What are your average monthly downloads?</label>
        <input type="text" class="form-control" id="inputAvgDownloads" name="inputAvgDownloads" aria-describedby="inputAvgDownloads" placeholder="Enter avg number of downloads">
      </div>
      <div class="form-group">
        <label for="inputDistributor">Who is your current podcast distributor?</label>
        <input type="text" class="form-control" id="inputDistributor" name="inputDistributor" aria-describedby="inputDistributor" placeholder="Enter name">
      </div>
      <div class="form-group">
        <label for="inputDAI">Are you using dynamic ad insertion for your podcasts?</label>
        <input type="text" class="form-control" id="inputDAI" name=" inputDAI" aria-describedby="inputDAI" placeholder="Enter response">
      </div>
      <div class="form-group">
        <label for="textHelp">How can we help you?</label>
        <textarea class="form-control" id="textHelp" name="textHelp" aria-describedby="textHelp" placeholder="Anything else you want to share?"></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
    </div>
  </div>
</div>
