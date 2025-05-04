---
layout: post
title: Wicked Features
description: How can we provide valuable features without slowing down shipping speed?
---

I was recently reading [Joy and Curiosity #38](https://registerspill.thorstenball.com/p/joy-and-curiosity-37-f50?publication_id=1543843&post_id=162747480&isFreemail=true&r=5dq9fb&triedRedirect=true) by Thorsten Ball, which linked to an [article](https://www.seangoedecke.com/wicked-features/) by Sean Goedecke coining the term "wicked feature". These are "features which must be considered every time you build another feature".

An example provided in the article was that of user types: if you introduce a premium subscription as a feature to your app, you must consider how premium users can interact with any new features you build. This certainly is a valuable feature, but it slows down development, as it adds an extra layer of complexity; a necessary check to tick off.

One of the things that makes a good engineer, the article continues, is the ability to "prevent your team from building wicked features where possible, and to limit the damage where the wicked feature must be built: by sensible refactoring". Or, more succinctly put by Goedecke:

> Good engineers limit the blast radius: they prevent unnecessary wicked features, and factor the necessary ones so they don’t pollute everything.

Here's a quick way I'd figure out whether a wicked feature is necessary: are there any paying users for this feature, and how much will that drive revenue growth? Once you've decided the wicked feature must be built, don't overengineer unless necessary. In the premium users example above, can a simple boolean field be added to the existing user schema, instead of creating an entirely new type?

That's also part of the reason veteran engineers at large tech companies are so valuable: they know all the wicked features in place, and know how the building of any new feature can break these requirements.
