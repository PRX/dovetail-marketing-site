---
layout: page
title: Opt Out of Programmatic Ad Targeting
description: You may opt out targeted programmatic advertising by any show on Dovetail.
permalink: /opt-out/
image: /assets/img/og-image.jpg
---
<header class="post-header bg-black-diagonal text-white lede hero px-5 pb-5 m-0">
  <div class="hero-content container col-xxl-8">
    <div class="hero-content-inner">
      <h1 class="display-5 post-title p-name" itemprop="name headline">Opt Out of Programmatic Targeting</h1>
    </div>
  </div>
</header>

<div class="p-5 bg-gray-x">
  <div class="container col-xxl-8">

  <div class="post-content">
    <p>You can opt out of your IP address being used for targeting in programmatic advertising in all shows hosted on Dovetail by filling out the form below.</p>
    <p>Opting out will not remove advertising, it does mean ads won't be targeted based on your IP address.</p>
    <p>This will only opt out the IP you are currently using; you will need to opt out each different IP, such as home and business IP addresses.</p>
    <p>All requests are reviewed by actual humans before being enacted, so please allow 2 weeks for them to take effect.</p>
    <p>We will opt out residential/static IP addresses indefinitely.<br>
    Mobile and transient addresses, since these are shared and change frequently, will be opted out for at least 60 days.</p>
    
    <hr/>
    {% if jekyll.environment == 'production' -%}
    <form name="opt_out_form" accept-charset="UTF-8" action="https://g26e6h83r5.execute-api.us-east-1.amazonaws.com/v1/submit" method="POST">
    {%- else -%}
    <form name="opt_out_form" accept-charset="UTF-8" action="https://dsmt2m9oj5.execute-api.us-east-1.amazonaws.com/v1/submit" method="POST">
    {%- endif %}
      <div class="form-group">
        <label for="inputEmail">Email address*</label>
        <input type="email" class="form-control" id="inputEmail" name="inputEmail" aria-describedby="emailHelp" placeholder="Enter email" required>
        <small class="form-text">Your email is required for verification purposes and, if necessary, to communicate with you about your opt out. We'll never share your email with anyone else.</small>
      </div>
      <div class="form-group">
        <label for="optOutIp">IP Address*</label>
        <input type="text" class="form-control" id="optOutIp" name="optOutIp" aria-describedby="optOutIp" required>
        <small class="form-text">We have retrieved your IP above, but you can also <a href="https://whatismyipaddress.com/" target="_blank">look up your IP here</a>. Once you submit the form, the IP address will be reviewed and then excluded. We'll never share your IP, and only use it for this opt out.</small>
      </div>
      <div class="form-group">
        <label for="textHelp">Comment</label>
        <textarea class="form-control" id="textHelp" name="textHelp" aria-describedby="textHelp" placeholder="Anything else you want to share?"></textarea>
      </div>
      <div class="cf-turnstile" data-sitekey="0x4AAAAAAAct7yXHEJttOvFy"></div>
      <input type="hidden" id="messageType" name="messageType" value="optOut" />
      <button type="submit" class="btn btn-primary">Submit Opt Out</button>
    </form>
    </div>
  </div>
</div>

<script>
  function getIP(data) { document.getElementById("optOutIp").setAttribute('value', data.ip); }
</script>

<script type="application/javascript" src="https://api64.ipify.org?format=jsonp&callback=getIP"></script>
