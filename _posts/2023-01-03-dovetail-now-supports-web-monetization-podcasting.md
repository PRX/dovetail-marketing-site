---
layout: post
permalink: /2023/01/03/dovetail-now-supports-web-monetization-podcasting
title: Dovetail now supports Web Monetization in Podcasting
author: Andrew Kuklewicz
image: /assets/img/web-mon-hero.png
heroimage: img/web-mon-hero.png
heroimagealt: Stylized Web Monetization icon
excerpt: Micropayments are a privacy safe alternative for unlocking additional producer revenue. We share how they work and how Dovetail supports them.

---

At PRX, we’ve been working on supporting micropayments for podcasting using [Web Monetization](https://webmonetization.org/). Web Monetization is a way to reward creators with real-time micropayments for their work while protecting privacy and supporting an open web. We see this as part of our larger goals to protect listener privacy and an open podcasting ecosystem.

With help from [Grant for The Web](https://www.grantfortheweb.org/), PRX built support for Web Monetization into our platform, and we are working with key creators to experiment with using these payments on their shows and websites, like "[_Song Exploder_](https://songexploder.net/)."

## Micropayments

In podcasting, and the internet in general, there are many ways to monetize: sponsorship, advertising, subscriptions, or for the lucky few, a book or movie deal. Still, every choice is a matter of trade-offs. Advertising costs attention and often entails tracking people’s internet activity (and thus, a loss of privacy). Subscriptions limit audiences and require signing up for yet another service. Movie deals…well, alright, that’s nice work if you can get it.

A still nascent form of monetization is micropayments. With micropayments, people sign up to reward creators based on their attention, and then creators receive a stream of payments when someone reads, views, or listens to their work online on a platform that enables payments. Micropayments are already happening with [Podcasting 2.0’s Value 4 Value](https://podcastindex.org/podcast/value4value), and many podcasters (> 10,000) have adopted micropayments using [Bitcoin over the Lightning network](https://podnews.net/article/how-to-earn-bitcoin-from-your-podcast).

But, for all the potential, the trade-off with micropayments is the technical and behavioral challenge of getting people to adopt the technology. To effectively adopt micropayments, you need consumers to sign up and enable payments, a way to know when content is consumed, *and* an affordable means to send payments. Ideally, all of this would be enabled to work on any website, anywhere, and not be limited by currency or vendor, and everyone would use it.

## Web Monetization

Web Monetization meets the technical challenges of micropayments. It is a [proposed standard](https://webmonetization.org/specification.html) with the W3C, the same international consortium that established all the major standards for the World Wide Web. Unlike other micropayment attempts like Value 4 Value that requires Bitcoin or [Brave that uses the Basic Attention Token (BAT)](https://brave.com/brave-rewards/), Web Monetization is not tied to a specific currency, implementation, or proprietary technology. Like other web technologies, it is based on standards that are meant to have many competing implementations, just as Mozilla, Google, and Microsoft all implement web standards in their own browsers. Another open standard that Web Monetization depends on is the [Interledger payments protocol](https://interledger.org/developer-tools/get-started/overview/), which is built for transferring payments between banks, ledgers, and currencies, allowing payments to flow without requiring any single payment provider or financial institution.

For example, if a person only wants to pay or receive traditional fiat currencies like USD, they can do so. The payments move through payment routers like data through a network, with defined start and end points, but no particular currency or payment provider required along the way, though in current implementations, they will often go through the [XRP Ledger](https://xrpl.org/), an open-source, low-cost, energy-efficient blockchain built for making micropayments.

Even with all these technical advantages, there is still the behavioral challenge to adopting Web Monetization by consumers, creators, and the technologists that build on these standards. To that end, the [Interledger Foundation](https://interledger.org/), [Mozilla](https://foundation.mozilla.org/en/campaigns/web-monetization/), [Creative Commons](https://creativecommons.org/2019/09/16/grant-for-the-web), [Interledger](https://interledger.org/), and [Coil](https://coil.com/), all recognizing that bootstrapping adoption of a new ecosystem is no small matter, and who together created [Grant for the Web](https://www.grantfortheweb.org/) to support this new open payments ecosystem.

## Getting Started for Creators and Audiences

For creators to get started, they need an online wallet, like an [Uphold](https://webmonetization.org/docs/uphold/) account, to receive money via the protocol that handles micropayments (i.e. [Interledger](https://interledger.org/developer-tools/get-started/overview/)).

With a wallet, they get a public address for receiving payments, something like the `@First-Lastname` addresses Venmo and similar (proprietary) services provide. Public addresses for Web Monetization are called [Payment Pointer](https://webmonetization.org/docs/ilp-wallets/#payment-pointers), and look something like `$ilp.uphold.com/ABC3DefGHijk`.

Much like an email address is how folks send messages to someone, this payment pointer is how they send payments to a creator. To use it, the address needs to be available and enabled where an audience pays attention to work on the web, and the audience needs to have set up paying for that work.

Wallets provide a way for a creator to receive payments, while a membership with [Coil](https://coil.com) (and [installing a browser extension](https://help.coil.com/docs/membership/coil-extension/index.html)) is how a fan can send money. Each Coil member who pays $5 a month supports web-monetized content with $0.36 per hour of attention. This may not sound like much, but it adds up, especially when compared to advertising. A thousand listens to a podcast, with three mid-rolls at a $20 CPM, would only pay $60, but if those same thousand listeners play 30 minutes of content, that’s $180.

Wallets and memberships are the two hands reaching out to make Web Monetization connect. When used in combination, if a [Coil](https://webmonetization.org/docs/getting-started#4-add-the-meta-tag-to-your-website) member visits monetized content, all a creator needs is [a single tag](https://webmonetization.org/docs/getting-started#4-add-the-meta-tag-to-your-website) on their site, link their [YouTube channel](https://help.coil.com/docs/monetize/content/youtube-monetize-channel/index.html), or add it to their PRX-hosted podcast to enable payments.

## Web Monetization with Dovetail

For podcasters using [Dovetail from PRX](/), it’s simple to get started with Web Monetization (and all explained in [this help article](https://help.prx.org/hc/en-us/articles/9901810244251-How-can-I-set-up-micropayments-for-my-podcast-)).

On any podcast in Dovetail, a producer can paste in a payment pointer address, hit save, and the feed will be updated to include the address and enable monetization:

{% picture img/web-mon-1.jpg --alt Setting up Web Monetization in Dovetail
 %}

### A Web Monetized Podcast Player
Adding the payment pointer to the feed is essential, but we also need podcast players to be Web Monetization enabled and make use of it. PRX also supports an open-source web player for podcasts, so we added support for web monetization in our own player, the very one used already by many of our podcasters like on "[_Song Exploder_](https://songexploder.net/)" and "[_Book Exploder_](https://bookexploder.com/)."

Now, when someone using web monetization listens to an episode on the [_Book Exploder_](https://bookexploder.com/episodes/james-mcbride) website, they will send payments while they listen, with the dollar sign icon showing that monetization is happening:

{% picture img/web-mon-2.png --alt An example PRX Player showing the monetization dollar sign in the bottom right corner
 %}

Clicking on the dollar sign icon shows a visualization for the streaming payments, and how much money has been sent while listening:

{% picture img/web-mon-3.png --alt The player showing payments streaming from the listener to the creator during playback %}

To make this work, Dovetail adds the payment pointer in a special tag in the RSS feed for the player to use to stream payments during playback. But we didn’t want to update the feed in a way that only works for PRX, we built on the work at the [Podcast Index defining monetization](https://github.com/Podcastindex-org/podcast-namespace/issues/132) in RSS, and further on how the folks at [Castopod built support for Web Monetization](https://blog.castopod.org/castopod-supports-web-monetization/). The result is a [Podcasting 2.0 proposal for a standard way to use web monetization for podcasting](https://github.com/Podcastindex-org/podcast-namespace/pull/409) that should work for any podcast host, and can be adopted by any podcast website or web player.

This is important, because when you believe in standards, it means working to support and bolster the work and inventions of others. As a practical result, it also means what we’ve built is interoperable, so with help from the team at [Castopod](https://blog.castopod.org/castopod-supports-web-monetization/), Castopod hosted podcasts can also receive payments from the open source PRX player.

For example, this Castopod hosted show "[Les Poésies d’Héloïse](https://lespoesiesdheloise.fr/@heloise)" can use the [PRX embeddable player](https://play.prx.org/e?uf=https://lespoesiesdheloise.fr/@heloise/feed.xml) to receive web monetized payments, just exactly like one hosted on Dovetail:

{% picture img/web-mon-4.png --alt A Castopod podcast with streaming payments in the PRX player %}

### What's Next?

As we advance an open podcasting ecosystem, we need more of the kind of collaboration and interoperability that standards provide and experiments to learn how best to use them.

As you might expect with experimental tech, there are still some limitations to how this works.

One shortcoming is that the current Web Monetization is really only for the web and isn’t integrated into mobile apps, which account for much of podcast listening. This is true of other types of media consumption as well and will eventually be addressed as the standards gain adoption.

Another is that payments only flow when the [browser is in the foreground](https://github.com/WICG/webmonetization/issues/17), which is perfect for text and video but not for audio. The equivalent for podcasts and music might be to stream payments when the sound is playing unmuted and loud enough to hear but unrelated to the browser focus or visual placement.

And the main limitation is not enough folks have [signed up to use Web Monetization to reward creators](https://coil.com/) for it to replace other sources of revenue.

If we want the future to be more equitable, open, and privacy safe, we have to be willing to experiment and work for it. We invite you all to [join us in this experiment](https://help.prx.org/hc/en-us/articles/9901810244251-How-can-I-set-up-micropayments-for-my-podcast-), [learn more](https://community.interledger.org/page/intro-to-web-monetization) about Web Monetization than this one post can convey, and think critically about how the choices we make affect creators, listeners, and the open web.
