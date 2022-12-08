---
layout: post
permalink: 2019/09/06/five-features-of-prx-metrics-we-want-to-you-to-know-about
title: Five features of PRX Metrics we want you to know about
author: Brandon Hundt
image: /assets/img/metrics-post-1.jpg
heroimage: img/metrics-post-1.jpg
heroimagealt: Podcast studio with microphone in foreground
excerpt: PRX’s Metrics platform empowers audio producers with download and audience data
canonical_url: https://medium.com/prxofficial/five-features-of-prx-metrics-we-want-to-you-to-know-about-f3aceb15b47b

---

<em>Note: This article was originally posted on <a href="https://medium.com/prxofficial/five-features-of-prx-metrics-we-want-to-you-to-know-about-f3aceb15b47b">PRX's company blog</a>.</em>

PRX’s <a href="https://www.prx.org/services/publishing-platform">publishing platform</a> is at the heart of our mission to serve audio creators. It allows producers to easily add new content and distribute it across an ever increasing list of listening apps and technologies (like smart speakers.)

In the past year, we’ve been working hard to further deliver on this mission by adding new features to Metrics, our in-house data platform that allows producers to see the impact of and audience for their stories. It shows all the unique downloads for podcast audio, from every platform and player, so that producers can realize their vision, take measurable risks, and make more meaningful media.

The tech team is proud of our recent work because of the value Metrics brings to producers. Here’s what Sandi Barr, PRX Senior Software Engineer and Metrics Champion™ says:

<blockquote>
  <em>It’s so important for podcasters to have access to and be able to make the most out of their data. The podcasts we carry on PRX are owned and managed by the users — independent producers, media companies, and public radio stations. We’re so proud that we can offer them a platform along with our guidance and leadership in the industry to help them better understand and make use of their data to grow their reach.</em>
</blockquote>

## How Metrics Works:

The glue of the PRX publishing platform is <a rel="noopener" href="/prxofficial/on-dovetail-618153c4d67e">Dovetail</a>, an application that seamlessly inserts sponsorship messaging with podcast episodes uploaded into our content management system, Publish. Also inserted into each episode by Dovetail is a pixel tracker that counts when an episode is streamed or downloaded.

Dovetail then provides the data in its API to Metrics, which displays it in a frontend built using Angular.

Note: PRX strongly believes in user privacy.<strong> </strong>All the pixel tracker collects are a count of the download, a timestamp, the user-agent reported from the app itself, and a portion of the IP address to report location.<strong> None of this can directly tie back to a single listener, meaning the listener is fully anonymous to our publishing platform.</strong> <strong>All we know is that somebody listened, not who.</strong> Furthermore, we do not collect any information on what other podcasts people may be listening to. What they listen to is their business, not ours.

I’d like to highlight 5 features of Metrics that empower creators.

<hr>

## 1) Near real time data updates and flexible time selection

{% picture img/metrics-body-1.png --alt screenshot of PRX Metrics date selection %}

Our producers can begin to track episode performance as soon as they publish an episode. Metrics has the latest data within minutes of a new listen being recorded by Dovetail, allowing producers to receive live updates of traffic on an episode.

Users can measure episode performance in custom time ranges based on the unique cadence of each show (daily, weekly, seasonality).

## 2) Drop day charts

{% picture img/metrics-body-2.png --alt screenshot of PRX Metrics drop day charts %}

Leveraging real time data, we built a Drop Day chart to help creators see for themselves how episodes compared to one another in the hours and days following an episode drop. This allows producers to better understand the timing of releasing podcast episodes.

For example, if a producer of a weekly podcast releases a podcast a few hours later than normal (or even a day later,) they can directly see the impact that the publishing delay may have on traffic, positive or negative.

## 3) Easily switch between your shows

{% picture img/metrics-body-3.png --alt show switcher %}

Many of the creators that use our publishing platform produce multiple podcasts, so we’ve provided easy ways to navigate between them.

## 4) Aggregated show downloads. You can see a single episode, or compare releases.

{% picture img/metrics-body-4.png --alt screenshot of PRX Metrics episode list %}

To this point, we’ve focused a lot on tracking individual episodes, but creators can also check data across a series of episode releases and export it to CSV or Google Sheets. Data is also rolled up to easily see how your selected range compares to the all-time stats for a show.

## 5) Information about where listeners are located, and the apps they use to hear your show

{% picture img/metrics-body-2.png --alt screenshot of PRX Metrics apps performance list %}

Previously, I mentioned how Dovetail’s pixel tracker collects some non-personally identifiable data. We report this to producers using Metrics through maps, charts and tables. Producers can look up listenership by country or metro area (DSM), as well as by device and the podcast app used — assuming the podcast app provides a user-agent we can use to track. This gives producers useful information to make marketing decisions regarding ad spend and promotion opportunities.

<hr>

To conclude, many folks played a part in the development of Metrics, but I’d like to single out three for a shout out: the aforementioned Sandi Barr, Technical Lead Ryan Cavis, and Director of Design Chris Kalafarski. 🌮 Tacos all around.
