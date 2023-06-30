---
layout: post
title:  "Necko News #1 - First Necko Newsletter"
date:   2021-09-27 14:45:00 +0200
categories: newsletter
author: Valentin Gosu
---

## Highlights

Valentin Gosu is now the module owner of [libjar](https://wiki.mozilla.org/Modules/All#libjar). Many thanks to Aaron Klotz for the great work maintaining this module in recent years. Kershaw Chang is now a peer of libjar.

Manuel Bucher has recently joined the team as a student worker based in Germany.

Dragana [refactored how necko drives TLS](https://bugzilla.mozilla.org/show_bug.cgi?id=1382886) handshakes and improved the CPU usage during 0RTT

## Friends of the Necko team

Glenn Strauss submitted a patch a while ago adding support for [SHA-256 Digest authentication](https://bugzilla.mozilla.org/show_bug.cgi?id=472823). Because the code touched by the patch was quite old this caused us to do a refactoring of the authentication code to bring it closer to the [Mozilla coding guidelines](https://firefox-source-docs.mozilla.org/code-quality/coding-style/coding_style_cpp.html) and add better tests.

Ping Chen (:rnons) fixed [Bug 1717185 - TCPSocket.send incorrectly returns true because mBufferedAmount is not updated in time](https://bugzilla.mozilla.org/show_bug.cgi?id=1717185)

## Project Updates

* HTTPS RR
  * [HTTPS RR](https://developer.mozilla.org/en-US/docs/Glossary/https_rr) shipped on release 92.
* Socket process
  * Dana is working on [bug 1712837](https://bugzilla.mozilla.org/show_bug.cgi?id=1712837) to make OS client certificates work with the socket process.
  * Kershaw made websocket work with the socket process. See [bug 1716566](https://bugzilla.mozilla.org/show_bug.cgi?id=1716566). 
* DNS over HTTPS
  + DoH shipped in Canada in Firefox 92
  + Manuel is adding support for [DNS padding](https://bugzilla.mozilla.org/show_bug.cgi?id=1543811) to mitigate traffic analysis

Nihanth is making our TRR implementation (Trusted-Recursive-Resolver) [fall back to unencrypted DNS less often](https://bugzilla.mozilla.org/show_bug.cgi?id=1714182)

Read this newsletter on [dev-platform](https://groups.google.com/a/mozilla.org/g/dev-platform/c/_hYnRM1DvRg/m/7kVA3a2gAgAJ)
