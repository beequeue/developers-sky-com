---
layout: post
title:  Bulk redirect testing for ExpressJS
date:   2016-02-08
author: Brendan Quigley (Solutions Architect - Digital Content)
categories: testing
excerpt: “Need to test a lot of routes in your NodeJS app?  Read on...”
---

In the Sky Digital Content tribe, one of our ongoing projects has been to roll out a responsive design across the [skysports.com](http://www.skysports.com) webiste.  In the past, mobile users had been redirected to a specific mobile site - m.skysports.com - but we eventually reached a point where the main site was responsive enough to deem this unecessary.  As such, the 'm' site's days were numbered...

### The project

We didn't want to abandon the many users of the 'm' site, who had faithfully bookmarked their favourite sport or team homepage, not to mention the swathes of existing links abounding on the internet.  Transitions like the one we were about to undertake should come as a pleasant surprise for the end-user, leaving them on an upgraded page with content they would expect - not a confusing catch-all, depositing them on a generic site homepage.

To that end, we set out to build an 'intelligent' redirector.  It would match on numerous static URLs, but also dynamic ones too.  It would map legacy URLs containing football team IDs to their SEO-friendly counterparts on the main site.  It would push URLs containing news article IDs through further redirection ensuring the user ended up on the much fresher responsive article page.  Before giving up, it would try to pattern-match which sport they unrecognised request was for, etc.  In short, it should make the switch as painless as possible for the user.

We decided that NodeJS would be a suitable candidate for this type of mass redirecting and of course we had testing in mind from the start.  We opted to use jasmine, as it is something of an in-house standard.  But how could we best go about thoroughly testing this redirect functionality?

### Part 1 - SuperTest

The first challenge was to set up expectations on the routing that we configured our express app to perform.  This could have been achieved by having traditional web-drivers like Selenium and friends make actual HTTP requests against a running instance of the app, then examining the responses for correctness.  This felt a little heavy-handed given the many hundreds of URLs we aimed to test.  Surely some way of isolating and testing the request/response functionality existed?  It did - SuperTest.

...

Now that we could efficiently test our routing, we needed an elegant way to bombard it with test cases.  So to the second challenge.

### Part 2 - jasmine-data-provider

Like the author of this very fine library, we have experience with PHPUnit and had identified the data provider pattern used there as the solution we were looking for.  A quick search for 'jasmine data provider' yields... yes you guessed it :).

...

## References

[Supertest](https://github.com/visionmedia/supertest)

[jasmine-data-provider](https://github.com/MortalFlesh/jasmine-data-provider)