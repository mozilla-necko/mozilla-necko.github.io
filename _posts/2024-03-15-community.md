---
layout: post
title: "Necko News #5 - Strengthening Community Involvement"
date: 2024-03-15 17:30:00 +0100
categories: newsletter
author: Manuel Bucher
---

## Highlights

* [Lars Eggert](https://www.eggert.org/), current chair of the Internet Engineering Task Force ([IETF](https://www.ietf.org/)), joined the Necko team. Welcome!
* Manuel presented [Debugging HTTP/3 upload speed in Firefox](https://fosdem.org/2024/schedule/event/fosdem-2024-1873-debugging-http-3-upload-speed-in-firefox/) on [Fosdem 2024](https://fosdem.org/2024/)
* If you are on [Chemnitzer Linux Tage 2024](https://chemnitzer.linux-tage.de/2023/en/) and want to meet up, please reach out to Manuel via [Email](mailto:manuel@mozilla.com) or [Matrix](https://matrix.to/#/@manuel:mozilla.org) and we can find a time to meet!
* We started publishing our [Weekly Meeting Notes](https://mozilla-necko.github.io/meeting-notes/) again. Subscribe [@Necko on mozilla.social](https://mozilla.social/@necko/) to get notified about new posts.
* We’re experimenting with Necko Office Hours. They are on the third Friday each month. The first one will be Friday, April 13, 15:00 - 16:00 CEST. Feel free to drop by if you are curious. It’s a place to talk and learn about Firefox networking. Ask in [#necko:mozilla.org](https://matrix.to/#/#necko:mozilla.org) if you want to join. We will announce the Office hours prior to the meeting in the channel too.

## Friends of Necko

We had quite a few new and known community members contribute to our Necko code base. We are happy about everyone that wants to get involved. Reporting bugs, submitting logs, and also patches are all highly valued by us. You can take a look at our [good-first-bugs](https://bugzilla.mozilla.org/buglist.cgi?component=DOM:%20Networking&component=Networking&component=Networking:%20Cache&component=Networking:%20Cookies&component=Networking:%20DNS&component=Networking:%20File&component=Networking:%20Proxy&component=Networking:%20HTTP&component=Networking:%20JAR&component=Networking:%20WebSockets&keywords=good-first-bug,%20&keywords_type=allwords&product=Core&resolution=---&order=Bug%20Number%20DESC) and also reach out to us at matrix [#necko:mozilla.org](https://matrix.to/#/#necko:mozilla.org) if you want to start getting more involved.

Setting up the toolchain can be quite challenging. Therefore, we sometimes have good-first-bugs that give you the opportunity to just test out the toolchain. In the past months Komuhangi Tumuhairwe ([Bug 1860231](https://bugzilla.mozilla.org/show_bug.cgi?id=1860231)) and ChaseKnowlden ([Bug 1862514](https://bugzilla.mozilla.org/show_bug.cgi?id=1862514)) took the opportunity and submitted patches for these bugs.

* Em Zhan implementing rel=modulepreload ([Bug 1798319](https://bugzilla.mozilla.org/show_bug.cgi?id=1798319))
* Greg Pappas [:gregp] on his initiative to [remove old prefs](https://bugzilla.mozilla.org/show_bug.cgi?id=1773039) removed a few Necko prefs and did other code cleanup
    * [Bug 1052909](https://bugzilla.mozilla.org/show_bug.cgi?id=1052909) - Remove network.websocket.auto-follow-http-redirects pref
    * [Bug 1819556](https://bugzilla.mozilla.org/show_bug.cgi?id=1819556) - Remove nsSocketTransportService::ProbeMaxCount
    * [Bug 1842173](https://bugzilla.mozilla.org/show_bug.cgi?id=1842173) - Remove network.http.clear_bogus_content_encoding pref
    * [Bug 1842326](https://bugzilla.mozilla.org/show_bug.cgi?id=1842326) - Remove `network.auth.use_new_parse_realm` and `network.auth.allow_multiple_challenges_same_line`
    * [Bug 1876945](https://bugzilla.mozilla.org/show_bug.cgi?id=1876945) - Run test_cookies_thirdparty.js and test_cookies_thirdparty_session.js with e10s enabled
    * [Bug 1883217](https://bugzilla.mozilla.org/show_bug.cgi?id=1883217) - Remove unused defines in IDL files
* Dr. Marten Richter reported and fixed both: 
    * [Bug 1872496](https://bugzilla.mozilla.org/show_bug.cgi?id=1872496) - Fix WebTransport's stream closure
    * [Bug 1873263](https://bugzilla.mozilla.org/show_bug.cgi?id=1873263) - Our WebTransport serverCertificateHashes Implementation
* Jackyzy823 landed and quickly fixed:
    * [Bug 1853203](https://bugzilla.mozilla.org/show_bug.cgi?id=1853203) - Support non-ASCII username/password for socks proxy
    * [Bug 1881883](https://bugzilla.mozilla.org/show_bug.cgi?id=1881883) - Nightly continuously outputs type=socks, flags=1
* Masatoshi Kimura [:emk] submitted a few patches to Necko:
    * [Bug 1875001](https://bugzilla.mozilla.org/show_bug.cgi?id=1875001) - Remove unused features from nsDirIndexParser
    * [Bug 1867229](https://bugzilla.mozilla.org/show_bug.cgi?id=1867229) - Remove unused fields from nsIDirIndex and nsIDirIndexParser
* Neel Chauhan [Bug 1861878](https://bugzilla.mozilla.org/show_bug.cgi?id=1861878) - Remove network.ssl_tokens_cache_use_only_once pref
* Jaydeep Das fixed the 18 years old [Bug 328707](https://bugzilla.mozilla.org/show_bug.cgi?id=328707) by allowing only valid IP/Hostname for Proxy Config
* Daisuke Akatsuka [Bug 1864985](https://bugzilla.mozilla.org/show_bug.cgi?id=1864985) - Add hasUserPass attribute to nsIURI
* CanadaHonk, who also contributed patches to Necko, [joined Mozilla](https://goose.icu/joining-mozilla/) in the DOM: Core team
* Max Inden has been very actively contributing to our http/3 implementation [neqo](https://github.com/mozilla/neqo/pulls?q=is%3Apr+author%3Amxinden). He is working closely with the Necko team. It’s a pleasure working with you.
* We had a few contribution from [Igalia](https://en.wikipedia.org/wiki/Igalia):
    * Mirko Brodesser landed a lot for [Bug 1797715](https://bugzilla.mozilla.org/show_bug.cgi?id=1797715) - Fetch Priority (previously known as [Priority Hints](https://wicg.github.io/priority-hints/))
    * Mirko Brodesser [Bug 1869488](https://bugzilla.mozilla.org/show_bug.cgi?id=1869488) - Log address of `nsIChannel` subobject of `nsHttpChannel` in the constructor/destructor too
    * Mirko Brodesser [Bug 1868802](https://bugzilla.mozilla.org/show_bug.cgi?id=1868802) - Add `this` pointer to `nsHttpHandler::NotifyObservers` logging
* From Redhat stransky migrated DbusWifiScanner to DBus/GIO ([Bug 1854449](https://bugzilla.mozilla.org/show_bug.cgi?id=1854449))

We’re sorry if we missed your contribution in this list. This list isn’t automatically generated, but we did go through our commit history by hand. Feel free to reach out on [#necko:mozilla.org](https://matrix.to/#/#necko:mozilla.org) and we'll add you in our next Newsletter.

## Project Updates

2023 has been a busy year with many started and completed project:

* Off main thread ([OMT](http://bugzilla.mozilla.org/show_bug.cgi?id=1528285)) for OnStopRequest was prototyped for HTML5Parser end of 2023 and [CSSLoader](https://bugzilla.mozilla.org/show_bug.cgi?id=1864817) begin of 2024
* URL Interop [2023](https://bugzilla.mozilla.org/show_bug.cgi?id=1815647) & [2024](https://bugzilla.mozilla.org/show_bug.cgi?id=1876105)
    * The 2023 interop effort saw us fixing several [high impact bugs](https://bugzilla.mozilla.org/show_bug.cgi?id=1815647) that brought our [URL interop score](https://wpt.fyi/interop-2023?feature=interop-2023-url) to 98.5% at the end of the year.
    * We had to disable [1603699 - Enable DefaultURI use for unknown schemes](https://bugzilla.mozilla.org/show_bug.cgi?id=1603699) after causing several issues with external protocol handlers. We are considering re-enabling this with an allow-list.
    * [1876105 - (interop-2024-url) Meta Interop 2024 URL](https://bugzilla.mozilla.org/show_bug.cgi?id=1876105) tracks all the work remaining to pass 100% of the URL WPT tests.
* [1852752 - Allow resolving HTTPS (or arbitrary record types) RR with native DNS (without TRR)](https://bugzilla.mozilla.org/show_bug.cgi?id=1852752) is currently enabled on Nightly for specific platforms (Windows 11, Linux, Android 10+). This allows resolving HTTPS records even when DNS over HTTPS is not used. This should increase the use of HTTP/3, HTTPS and ECH. 

## Below the fold

* We [increased the number of threads used for DNS](https://bugzilla.mozilla.org/show_bug.cgi?id=1753979) resolution from 8 to 64. This reduced the waiting time from 26ms to 3ms in the 95th percentile, and from 816ms to 345ms in the 99th percentile.
* Devtool improvements:
    * [Bug 1870580](https://bugzilla.mozilla.org/show_bug.cgi?id=1870580) Netmonitor doesn’t show resources loaded from a file url
    * [Bug 1156659](https://bugzilla.mozilla.org/show_bug.cgi?id=1156659) - Simulating offline mode for a tab
    * [Bug 1820807](https://bugzilla.mozilla.org/show_bug.cgi?id=1820807) Authentication requests were not visible in devtools
* We [improved our DoH telemetry](https://bugzilla.mozilla.org/show_bug.cgi?id=1784257) to get alerts about our DoH outages
* [Early Hints preconnect](https://bugzilla.mozilla.org/show_bug.cgi?id=1858712) was enabled in [Fx120](https://whattrainisitnow.com/release/?version=120)
* [Early Hints preload](https://bugzilla.mozilla.org/show_bug.cgi?id=1874445) was enabled in [Fx123](https://whattrainisitnow.com/release/?version=123)
* We had our second Bug Bash Session giving our backlog a fresh view. This time we
    * Updated [210](https://bugzilla.mozilla.org/buglist.cgi?chfieldfrom=2024-02-23&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets&chfieldto=2024-02-24&query_format=advanced&product=Core&list_id=16913244&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other) bugs in total
        * Closed: [69](https://bugzilla.mozilla.org/buglist.cgi?chfield=cf_last_resolved&chfieldfrom=2024-02-23&product=Core&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets&list_id=16913246&query_format=advanced&chfieldto=2024-02-24)! (including some Meta bugs)
            * S3: [48](https://bugzilla.mozilla.org/buglist.cgi?bug_severity=S3&chfieldfrom=2024-02-23&query_format=advanced&list_id=16913480&chfield=cf_last_resolved&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets&product=Core&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other&chfieldto=2024-02-24) (Total S3 reduced by 2.6%)
            * S4: [3](https://bugzilla.mozilla.org/buglist.cgi?chfieldto=2024-02-24&list_id=16913481&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other&chfield=cf_last_resolved&bug_severity=S4&query_format=advanced&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets&chfieldfrom=2024-02-23&product=Core)
            * NA: [18](https://bugzilla.mozilla.org/buglist.cgi?query_format=advanced&chfieldfrom=2024-02-23&chfield=cf_last_resolved&list_id=16913484&bug_severity=N%2FA&chfieldto=2024-02-24&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other&product=Core&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets)
        * Priority/severity updated: [20](https://bugzilla.mozilla.org/buglist.cgi?product=Core&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other&chfieldto=2024-02-24&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets&chfield=priority&chfield=bug_severity&list_id=16913252&query_format=advanced&chfieldfrom=2024-02-23)
        * Blocks updated: [73](https://bugzilla.mozilla.org/buglist.cgi?query_format=advanced&chfieldfrom=2024-02-23&chfield=blocked&list_id=16913464&product=Core&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other&chfieldto=2024-02-24&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets)
        * Necko Priority Queue: 2 added 
        * Necko Next: 68 (added 19)
        * Necko Priority Review: down to 16
    * Assigned owners to our Meta bugs owners [meta bugs](https://bugzilla.mozilla.org/buglist.cgi?list_id=16940437&product=Core&keywords_type=allwords&resolution=---&query_format=advanced&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&keywords=meta&component=DOM%3A%20Networking&component=Networking&component=Networking%3A%20Cache&component=Networking%3A%20Cookies&component=Networking%3A%20DNS&component=Networking%3A%20File&component=Networking%3A%20HTTP&component=Networking%3A%20JAR&component=Networking%3A%20Proxy&component=Networking%3A%20WebSockets&classification=Client%20Software&classification=Developer%20Infrastructure&classification=Components&classification=Server%20Software&classification=Other)

You can send feedback regarding this Newsletter to [necko@mozilla.com](mailto:necko@mozilla.com) and discuss on [dev-platform](https://groups.google.com/a/mozilla.org/g/dev-platform/c/Ytr6DpwBISw).
