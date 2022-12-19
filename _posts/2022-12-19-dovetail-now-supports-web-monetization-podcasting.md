---
layout: post
permalink: /2022/12/19/dovetail-now-supports-web-monetization-podcasting
title: Dovetail now supports Web Monetization in Podcasting
author: Andrew Kuklewicz
image: /assets/img/web-mon-hero.png
heroimage: img/web-mon-hero.png
heroimagealt: Stylized Web Monetization icon
excerpt: Micropayments are a privacy safe alternative for unlocking additional producer revenues. We share how they work and how Dovetail supports them.

---

When we started out almost 20 years ago, PRX launched [a marketplace for independent audio makers](https://www.prx.org/exchange) to get paid for their work, and while we've grown and evolved to do [just a few more things](https://2021.prx.org/), we’re always looking for more ways to support creators.

Now in podcasting, and the internet in general, there are many ways to monetize (sponsorship, advertising, subscriptions, or for the lucky few a book or movie deal), but every choice is a matter of trade-offs. Advertising often entails tracking and a loss of privacy. Subscriptions limit audiences and require signing up for yet another service. Movie deals…well, alright, that’s nice work if you can get it.

A still nascent form of podcast monetization is micropayments. With micropayments, people sign up to reward creators whose work they seek out online, then creators receive a stream of payments whenever someone reads, views, or listens to their work online. This is already happening with [Podcasting 2.0's Value 4 Value](https://podcastindex.org/podcast/value4value), and many podcasters have adopted Value 4 Value using [Bitcoin over the Lightning network](https://podnews.net/article/how-to-earn-bitcoin-from-your-podcast) to get paid from apps and listeners that support it (i.e. used by over 10,000 at the time this was written).

Pardon the pun, but micropayments are worth paying attention to, both as a privacy safe alternative to advertising, and fulfilling the long standing goal of linking listener support to what they actually value with their attention, [a direction we’ve explored before](https://blogs.harvard.edu/doc/2010/07/19/listenlog/).

But, for all the potential, the trade-off with micropayments are the technical and behavioral challenges to adoption. You need consumers to sign up and enable payments, a way to know when content is consumed, and then a means to send those payments. Ideally all of this would work on any website, anywhere, not limited only to a single site or vendor. How might we get enough people to use such standard technologies to replace the revenue that comes from surveillance heavy advertising?

At PRX we've been working on how to support micropayments for podcasting using the [Web Monetization standard](https://webmonetization.org/). Why work on Web Monetization? Well, firstly it is a [proposed W3C standard](https://webmonetization.org/specification.html), not tied to a specific currency, implementation, or proprietary technology. It’s also based on the [Interledger payments protocol](https://interledger.org/developer-tools/get-started/overview/), which is built for routing payments between banks, ledgers, and currencies.

For example, if a person only wants to pay or receive traditional fiat currencies like USD, they can do so. The payments move through payment routers like data through a network, with no particular currency or payment provider required along the way, though often through the [XRP Ledger](https://xrpl.org/) which is an open source, low-cost, energy efficient blockchain built for making micropayments.

Because Web Monetization and the technologies used to build it are all based on standards, no one has to and the goal is to make this ubiquitous and frictionless as the other common standards built into our browsers and devices. To that end, it is backed by [Mozilla](https://foundation.mozilla.org/en/campaigns/web-monetization/), [Creative Commons](https://creativecommons.org/2019/09/16/grant-for-the-web), [Interledger](https://interledger.org/), and [Coil](https://coil.com/), all recognizing that bootstrapping adoption of a new ecosystem is no small matter, and who together created [Grant for the Web](https://www.grantfortheweb.org/) to support this new open payments ecosystem.

Nothing could be closer to our values than working towards an open web that is privacy safe and rewards creators, just as we work to protect listener privacy and an open podcasting ecosystem.

## That's all well and good, but you may be asking how can I get started?
For podcasters using Dovetail, it's simple (and all explained in [this help article](https://help.prx.org/hc/en-us/articles/9901810244251-How-can-I-set-up-micropayments-for-my-podcast-)).

First you need an online wallet to receive money via the protocol that handles micropayments (i.e. [Interledger](https://interledger.org/developer-tools/get-started/overview/)), for example by [opening an account on Uphold](https://webmonetization.org/docs/uphold/).

With a wallet, you also get a public address for receiving payments, something like what you may be used to with Venmo and similar (proprietary) services. For Web Monetization, these are called [Payment Pointers](https://webmonetization.org/docs/ilp-wallets/#payment-pointers), and look like `$ilp.uphold.com/ABC3DefGHijk`.

Much like an email address is how folks send you messages, this address is how they can send you payments. To use it, the address needs to be set-up where your audience pays attention to your work on the web.

For example, to get paid $0.36 per hour of attention when a [Coil](https://coil.com/) member visits your website, all you need to do is [add a single tag](https://webmonetization.org/docs/getting-started#4-add-the-meta-tag-to-your-website), or link that same pointer to your [YouTube channel](https://help.coil.com/docs/monetize/content/youtube-monetize-channel/index.html), or now add it to your PRX hosted podcast.

In Dovetail, we now offer options both for linking to a donation form and for providing a micropayments address. Simply paste in your wallet's payment pointer address, hit save, and your feed will be updated to include the payment pointer address:

{% picture img/web-mon-1.jpg --alt Screenshot of Engagement Settings tab within Dovetail %}

Adding the payment pointer to the feed is half the solution, we also need podcast players to make use of it. PRX also supports an open source web player for podcasts, so we added support for web monetization in our player, the very one used already by many of our podcasters like “[Song Exploder](https://songexploder.net/)”.

Now, when someone using web monetization listens on https://songexploder.net/, they will send payments while they listen, with the dollar sign icon showing that monetization is happening:

{% picture img/web-mon-2.png --alt Screenshot of PRX audio player with web monetization turned on %}

And if you click on it, showing how much money has been sent while listening:

{% picture img/web-mon-3.png --alt Screenshot of PRX audio player showing how much money the producer earns from a web monetized visitor %}

How this works is that we’ve added the payment pointer in a special tag in the RSS feed for the player to find and use to stream payments while the audio plays. But we didn’t want to update the feed in a way that only works for PRX, we built on the work the Podcast Index folks used to define Value4Value payments in RSS, and further on how the folks at Castopod built support for Web Monetization. The result is a [Podcasting 2.0 proposal](https://github.com/Podcastindex-org/podcast-namespace/pull/409) for a standard way to use web monetization for podcasting.

When you create a standard, it means working to support and bolster the work and inventions of others. It means what we’ve built is interoperable, so with help from the team at [Castpod who implemented support for Web Monetization](https://blog.castopod.org/castopod-supports-web-monetization/), a Castopod feed can also receive payments from the open source PRX player.

For example, this Castpod hosted show “[Les Poésies d’Héloïse](https://lespoesiesdheloise.fr/@heloise)” can use the [PRX embed player](https://play.prx.org/e?uf=https://lespoesiesdheloise.fr/@heloise/feed.xml) to receive web monetized payments, just exactly as one hosted on Dovetail:

{% picture img/web-mon-4.png --alt Screenshot of PRX embed player, playing the Castpod hosted show “Les Poésies d’Héloïse” %}


What do we do next? As you might expect with new tech, there are some limitations still to how this all works.

One shortcoming is that the current Web Monetization is really only for the web, and isn’t integrated into apps, which account for much of podcast listening.

Another is that payments only flow when [the browser is in the foreground](https://github.com/WICG/webmonetization/issues/17), which is perfect for text and video, but not for audio, where the equivalent is when the sound is playing unmuted/loud enough to hear.

And the main limitation is not enough folks [have signed up to use Web Monetization to reward creators](https://coil.com/) for it to replace other sources of revenue.

If we want the future to be more equitable, open, and privacy safe, we have to be willing to experiment and work for it. I invite you all to [join us in this experiment](https://help.prx.org/hc/en-us/articles/9901810244251-How-can-I-set-up-micropayments-for-my-podcast-), learn more about [Web Monetization](https://webmonetization.org/) than this one post can convey, and think critically about how the choices we make affect creators, listeners, and the open web.
