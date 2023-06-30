---
layout: post
title:  "Necko News #2 - Season's greetings"
date:   2021-12-23 18:00:00 +0200
categories: newsletter
author: Dragana Damjanovic
---

Season’s greetings! 

The Necko team is pleased to provide an early Christmas present with our second newsletter! :-)

## Highlights

Greg Hess has recently joined Mozilla as the new Necko team manager bringing 20yrs experience in software development. He was born a developer(Java first love) and followed a technical track moving on to team lead, client architect and technical director before entering management/agile coaching. He has a broad range of market experience developing web and mobile applications for SaaS hosting, Home Media Servers, Premium Online TV, Aviation and Defense, Digital Marketing and Social Media. Some notable projects he has worked on are Netgear Stora, Disney Channel(CA), Cartoon Network(US-2016 Emmy award), Barbie.com and McDonalds Happy Studio(EU).

## Project Updates

* HTTP3
  * Dragana has added WebTransport support to neqo
  * Manuel added the HTTP priority extension. This is enabled on [Beta](https://bugzilla.mozilla.org/show_bug.cgi?id=1734132)
* Socket process
  * Kershaw moved the evaluation of PAC scripts into the socket process. This is currently enabled on [Nightly](https://bugzilla.mozilla.org/show_bug.cgi?id=1745385)
  * Kershaw made it possible to [generate the connection info asynchronously](https://bugzilla.mozilla.org/show_bug.cgi?id=1739001) for TRR channels in the socket process 
* DNS over HTTPS (Trusted-Recursive-Resolver)
  * Nihanth implemented a [retry mechanism for TRR requests.](https://bugzilla.mozilla.org/show_bug.cgi?id=1737198)
  * Valentin fixed a bug that caused some [DNS queries to be leaked to the native DNS resolver](https://bugzilla.mozilla.org/show_bug.cgi?id=1566998) when resolved by WebRTC.
  * [DNS padding](https://bugzilla.mozilla.org/show_bug.cgi?id=1543811) shipped on release 95

## Below the fold

* The Necko team re-triaged all of our unassigned P2 bugs - some of them became P3 and some of them received some much needed attention.
* Valentin is working on [purging the HTTP cache in a background task during shutdown](https://bugzilla.mozilla.org/show_bug.cgi?id=1705676). This should get rid of some annoying [shutdown](https://bugzilla.mozilla.org/show_bug.cgi?id=1356853) [hangs](https://bugzilla.mozilla.org/show_bug.cgi?id=1682899) on windows.
* Authentication challenges are now [sorted by their safety rating](https://bugzilla.mozilla.org/show_bug.cgi?id=650091) instead of the order they’re sent by the server.
* Dragana and Manuel have started work on [103 Early Hints](https://bugzilla.mozilla.org/show_bug.cgi?id=1407355)

We would like to wish you all a happy and healthy holiday season!

- Necko Team

Read this newsletter on [dev-platform](https://groups.google.com/a/mozilla.org/g/dev-platform/c/QbIZTTUlrIQ/m/8L7YEu_kDQAJ)
