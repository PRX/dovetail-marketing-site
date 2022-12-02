---
layout: post
permalink: /2022/12/02/dovetail-glossary
title: Dovetail Glossary
author: Ryan Cavis
image: /assets/img/hero-features.jpg
heroimage: /img/hero-features.jpg
heroimagealt: Podcasting studio with microphone in foreground
excerpt: Commonly used podcasting terms and definitions used throughout Dovetail from PRX

---

## Podcast Metrics

**Download:** A podcast episode download. As defined by the [IAB 2.1 Podcast Measurement guidelines](https://iabtechlab.com/wp-content/uploads/2021/03/PodcastMeasurement_v2.1.pdf), a listener must download enough of the episode creative file for 1-minute of audio to be counted.

**Impression:** A podcast ad impression. Also defined in the [IAB 2.1 Podcast Measurement guidelines](https://iabtechlab.com/wp-content/uploads/2021/03/PodcastMeasurement_v2.1.pdf), the listener must have downloaded all of the bytes in the episode creative file where the ad can be heard to be counted.
_Also see: “Actual”_

## Podcast Layouts

**Placements:** The configured layouts of a podcast’s audio segments. Each is made up of a list of Zones. If there are no placements configured for an audio template, vanilla/ad-free audio will be served.
Example: [Preroll1 Preroll2 Original1 Midroll Original2 Postroll]

**Zone:** A single audio segment within an episode, including both original and ad segments.
_Example: House Preroll 2_

**Section:** A grouping of consecutive ad Zones into a single block. May also distinguish between “paid” and “house” ads.
_Example: Preroll (containing both Preroll1 and Preroll2)_

## Ad Serving

**Campaign:** Represents an Inventory Order (IO) for a single advertiser. It can contain many Flights.

**Flight:** One or more creatives plus a set of targeting information to serve with a podcast. Configured with Zones, a date-range, and an Impression goal.
Ads are fulfilled by reserving Allocations against future Inventory.

**Creative:** Refers to the audio file (MP3, WAV, FLAC) or VAST URL containing the ad content.

**VAST:** An acronym that stands for Video Ad Serving Template. VAST is a way for multiple ad servers to communicate and serve ads, replacing individual ad audio files for a campaign with a VAST URL.

**Forecast:** The daily forecasted Downloads we expect a podcast to receive in the future. May also be broken out by Episode, Country, State, Keywords, etc.

**Inventory:** The daily number of Impressions available for ad Zones to be sold into in the future. (Equal to the Forecast multiplied by the ad Placements - original segment Zones do not get Inventory).

**Allocations:** The daily Inventory counts reserved by a Flight. May include additional targeting info such as Episode, Country, State, Keywords, etc.

**Availability:** The amount of unreserved Inventory left in the system (subtract the Allocations for whatever days/targeting you’re looking at).

**Actuals:** The number of real Impressions a flight has already received.
