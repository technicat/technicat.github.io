---
layout: post
title: I'm Shipping Dead Code
date: '2011-11-03T12:28:10-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515789246/im-shipping-dead-code
---
I’ve started updating all my [iOS apps](http://fugugames.com/) to require iOS 4.3 minimum. The official reason is to streamline my productivity and concentrate on taking advantage of the more powerful hardware and advanced features of the more recent generations of devices. The real reason is that the latest version of XCode keeps complaining that it can’t recognize my old 2nd-gen iPod touch, so I just gave up and decided to stop supporting it.

One would think that I could have done that by replacing my current “universal” armv6+armv7 builds with armv7-only builds from now on, excluding the 1st and 2nd-gen devices that use armv6 processors, and the nice thing about that is that I can cut down my build size and maybe get some more apps under the 20MB phone-connection download limit. But no, I discovered that switching to an armv7-only build adds “armv7” to the UIRequiredDeviceCabilities list in the Info.plist file and then when you submit the app, ITunesConnect will admonish you that you cannot add new required device capabilies to an existing app.

So instead, I’m still building for both armv6 and armv7, but requiring iOS 4.3, which accomplishes the same thing, since 2nd-gen devices stopped at iOS 4.2 (but this may inhibit people who have newer devices but don’t feel like upgrading to iOS 4.3)., But now I’m shipping dead code.

