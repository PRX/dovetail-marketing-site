---
layout: page
title: Contact
permalink: /contact/
---
<div class="bg-ltblue px-4 py-5 text-white border-top" id="icon-grid">
  <div class="container col-xxl-8">

  <header class="post-header">
    <h1 class="post-title">{{ page.title | escape }}</h1>
  </header>

  <div class="post-content">
    <p>Use this form to let us know how we can help you with your podcasting needs:</p>
    <hr />

    <form>
      <h2>Tell us a little about yourself...</h2>
      <div class="form-group">
        <label for="inputName">Name</label>
        <input type="text" class="form-control" id="inputName" aria-describedby="inputName" placeholder="Enter your name">
      </div>
      <div class="form-group">
        <label for="InputEmail1">Email address</label>
        <input type="email" class="form-control" id="InputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
        <small class="form-text text-white">We'll never share your email with anyone else.</small>
      </div>
      <div class="form-group">
        <label for="textOrganization">Organization</label>
        <input type="text" class="form-control" id="inputOrganization" aria-describedby="textOrganization" placeholder="Enter your organization">
      </div>
      <div class="form-group">
        <label for="textJobTitle">Job Title</label>
        <input type="text" class="form-control" id="textJobTitle" aria-describedby="textJobTitle" placeholder="Enter your job title">
      </div>
      <div class="form-group">
        <label for="textPhone">Phone Number</label>
        <input type="text" class="form-control" id="textPhone" aria-describedby="textPhone" placeholder="(xxx)-xxx-xxxx">
      </div>
      <hr />
      <h2>Tell us about your podcasts...</h2>
      <div class="form-group">
        <label for="NumberPodcasts">How many podcasts do you currently have?</label>
        <input type="text" class="form-control" id="NumberPodcasts" aria-describedby="NumberPodcasts" placeholder="Enter number of podcasts">
      </div>
      <div class="form-group">
        <label for="AvgDownloads">What are your average monthly downloads?</label>
        <input type="text" class="form-control" id="AvgDownloads" aria-describedby="AvgDownloads" placeholder="Enter avg number of downloads">
      </div>
      <div class="form-group">
        <label for="howHelp">How can we help you?</label>
        <textarea class="form-control" id="howHelp" aria-describedby="howHelp" placeholder="Anything else you want to share?"></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>

    </div>
  </div>
</div>
