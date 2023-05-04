---
layout: post
permalink: /2022/07/21/introducing-dovetail-as-product
title: Introducing Inventory Management in Dovetail from PRX
author: Brandon Hundt
image: /assets/img/homepage-hero.jpg
heroimage: img/homepage-hero.jpg
heroimagealt: Podcast studio with microphone in foreground
excerpt: Understand your inventory with best in class inventory management.
---

Over the past year, PRX carefully migrated our podcasts to our latest version of Dovetail - that now includes end to end ad inventory management.

Our Advertising Operations (Ad-Ops) team is now able to manage advertising campaigns from front to end in one system, including near real-time forecasts and availability broken down by Geo-targets available as the inventory order (IO) is being inserted.

Dovetail is a podcasting post-production suite of applications that excels in delivering dynamically inserted content, including the original audio files and ad creatives to your intended audience in a privacy conscious way.

## Why we added inventory management into Dovetail

For many years at PRX, we’ve been using dynamic ad insertion to ensure that ads were properly inserted into podcasts. As shows were published into PRX Publish, our APIs connected to a third party ad service (Kevel) and a script we wrote “Dovetail” rearranged the mp3 files into the desired order.

Building your own ad server is really hard. So by using Kevel we could lean on really good technology out of the box. As our CTO, Andrew Kuklewicz, points out in [an interview](https://soundsprofitable.com/article/kevel) with _Sounds Profitable_ host Bryan Barletta, the initial integration wasn’t very difficult and at the time made sense.

<iframe width="560" height="315" src="https://www.youtube.com/embed/CkZfvubCfSE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

However, after hundreds of millions, maybe billions, of ad impressions later, we learned we needed to be more efficient in our process. We really didn’t have a ton of visibility into the full inventory picture and it was difficult to forecast potential availability.

PRX’s Ad-Ops team did some serious spreadsheet magic to help manage the inventory. But a very large volume of inventory caused managing the sheets a challenge to manage. Quickly, the spreadsheet became so complex that it hit the limit of cells available in Google Sheets - something I wasn’t aware was realistically possible.

We were not certain if this was something to celebrate or if it was a cry for help. Certainly, the spreadsheet skills of our scrappy Ad-Ops team is undeniable and worthy of celebration - as they have worked tirelessly to successfully serve millions of ads in our podcasts in a month.

But there had to be a better way, a more efficient way that doesn’t rely on Google Sheets to track our ad inventory.

Consider forecasting. This well built spreadsheet was unable to keep up with changes and segments that would allow us to forecast future downloads without huge confidence buffers.

In other words, we have been leaving money on the table - money that the bulk of, goes back into the hands of our independent producers to create fine podcasts.

At PRX, we embrace the principles of design thinking and user centric design in building out our tech products. One of the central tenets of design thinking is fully understanding the needs of a single user and designing a product that fits their needs. In our case our user is the PRX Ad-Ops team.

If we correctly assume that the needs of the PRX Ad-Ops team are the same needs of other Ad-Ops teams in podcasting, then we have a product that would be helpful to independent podcasters across the industry.

So we, the PRX tech team, after hearing the cries of our Ad-Ops team started to work hand in hand with our Ad-Ops teams to consider how we could simplify the process of ad inventory management by solving for two goals, as outlined above:

1. Developing a better forecast of podcast performance
2. Retiring the Google Spreadsheet

## Forecasting

To more accurately forecast, we started by adding a Production calendar feature into our Dovetail Publish CMS and encouraging producers to add drafts of when they know future episodes will drop - even if its only a date in the future.

{% picture img/dovetail/1-production-calendar.png --alt screenshot of the production calendar in Dovetail %}

In addition, we also have a lot of IAB compliant data on how well our podcasts have performed historically. This data is made available in our Dovetail Metrics platform.

<strong>_Related: [Here are five features in Metrics we want you to know about](https://medium.com/prxofficial/five-features-of-prx-metrics-we-want-to-you-to-know-about-f3aceb15b47b)_</strong>

Knowing when episodes will drop and how they’ve performed historically allows us to predict how well we think a podcast is going to perform with some reliability using the statistical programming language R.

Here’s an example of one of the R generated forecasts:

{% picture img/dovetail/2-forecast.png --alt screenshot of a forecast in Dovetail %}

There are variables to accuracy, like how new a show is, or how often a show publishes - for example we’ve found that podcasts that drop daily are much easier to predict. This will give our Ad-Ops team more confidence on how aggressively a show can be sold.

Our forecasts are also flexible enough to handle some more advanced targeting based on IAB 2.0 compliant and privacy focused segmented audience data, like location.

_NOTE: As of May 1, 2023, PRX is now IAB certified._

## Inventory Order Input

Early in the process of building out inventory management capabilities we identified benchmarks for shows by the complexity of their advertising needs. We knew we couldn’t retire the aforementioned Inventory spreadsheets until we moved all of our podcasts over to the new system, helping us to identify the features we absolutely needed to have vs those we didn’t right away.

The first thing we identified is that we needed to ensure that our Ad-Ops team had a simple and easy to use application in which they can quickly add new IOs and segment them as they need.

{% picture img/dovetail/3-flight-form.png --alt screenshot of campaign and flight entry in Dovetail %}

What we think is the best feature of the campaign insertion form is the near real time forecasts available as you target ad zones within the podcast.

We also created a dashboard that allows campaign managers to quickly view and filter campaigns and flights to more easily manage and track the orders that have already been added.

## Availability at a Glance

PRX has a strong partnership with Market Enginuity for our podcast ad sales. One critical element of replacing the inventory spreadsheets was to create a simple view for Account Executives to quickly look up availability.

Therefore, we’ve built a dashboard that does just that. Look up availability:

{% picture img/dovetail/4-avails-search.png --alt screenshot of availability search in Dovetail %}

## Our Commitment to Listener Privacy

PRX is strongly committed to listener privacy. We are IAB 2.0 compliant, we only store a quartile of an IP address and we don’t track what you listen to -- only that someone downloaded a podcast.

PRX believes that the future of digital ads is in contextual advertising; where advertisers buy ads against content, not listeners. This will help keep more money in the pockets of our producers - allowing them to create more engaging content that you want to listen to.

Within Dovetail, we are continuing to improve our platform to increase content tagging capabilities and discoverability.

{% picture img/dovetail/6-category-blocks.png --alt screenshot of Brand Safety category selection in Dovetail %}

## Privacy-forward Programmatic Advertising

While we believe in the future of contextual advertising, there are use cases in which it makes sense to carefully use programmatic advertising exchanges to help our producers. For example, we have a large show with a large international audience, and programmatic is a way to help fill availability inventory.

We also have a lot of small shows or new shows that may be considered too small to sell ads into directly. In this case, programmatic ads can really help a show get off the ground floor.

VAST tags are becoming a standard in podcasting to request programmatic ads. We’ve worked with AdsWhizz to create a way to use VAST, while protecting listener privacy. This may mean that we won’t have access to all of the exchanges that exist, or have the ability to target listeners in all the ways possible, and that is fine by us. We want to vet and understand the sources for the ads our listeners receive.

Fortunately, our partners at Market Enginuity have created a privacy forward programmatic ad exchange that we can pull ads from to help producers.

{% picture img/dovetail/5-vast.png --alt screenshot of a VAST creative in Dovetail %}

## Self-Service Dovetail

We made a bet that our Ad-Ops team handles the same use cases that Ad-Ops teams across podcasting and outside of PRX come across on a near daily basis. This is a professional tool for professionals that respect user privacy and helps grow producer revenue. This may be the tool you need to grow your shows. If so, feel free to reach out us.
