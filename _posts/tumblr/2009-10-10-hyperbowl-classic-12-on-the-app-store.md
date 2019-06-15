---
layout: post
title: HyperBowl Classic 1.2 on the App Store
date: '2009-10-10T13:54:32-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318392371/hyperbowl-classic-12-on-the-app-store
---
After one week and five days (getting a little faster!), the latest [HyperBowl Classic update](http://itunes.com/app/hyperbowlclassic) has been approved on the App Store.

![IMG_0209](http://itshardtofondlepenguins.com/wp-content/uploads/2009/10/IMG_0209.png "IMG\_0209")

Besides the new end-of-game trophy scene, this fixes that embarrassing ninth-frame spare crash bug (two words: “global variable”) and has improved physics - pins fall completely, ball doesn’t get stuck in the wall.

That last one actually required a huge revamping - as I explained earlier in the blog entry on the [widget update](http://www.apple.com/downloads/dashboard/games/hyperbowlclassic.html), I first imported the HyperBowl assets into the [Unity engine](http://unity3d.com/) using the default scale settings which for some legacy reason is 0.01, and instead of reimporting them with an adjusted scale, I scaled all the physics settings down accordingly. Which is supposed to work, but apparently doesn’t. So I reimported and reattached everything for the widget and web player versions, and since the current version of Unity iPhone doesn’t seem to import that version of FBX, I reconverted the desktop version of HyperBowl Classic to Unity iPhone again. Which is probably for the best, keeping the desktop and iPhone versions close, but which means I have to reapply all the iPhone optimizations again (probably missed a few - oh, well, next update…)

In the meantime, we’re starting to see some decent reviews on the App Store page. Even the one-star review is actually a positive review - the user is just miffed that I updated the OS requirement to OS 3.0.

![Picture 7](http://itshardtofondlepenguins.com/wp-content/uploads/2009/10/Picture-7.png "Picture 7")

