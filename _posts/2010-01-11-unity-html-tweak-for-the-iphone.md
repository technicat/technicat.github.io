---
layout: post
title: Unity HTML Tweak for the iPhone
date: '2010-01-11T14:33:39-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318414001/unity-html-tweak-for-the-iphone
---
It was really bugging me that the Install Unity badge was appearing when I visited the [HyperBowl](http://hyperbowl3d.com/) page on my iPod touch. Of course, clicking (tapping) on it isn’t going to do anything useful. The basic problem is that the default HTML generated for Unity web players assumes that if the web player isn’t installed, you can install it (there was an exception for the incompatibility with 64-bit Safari running on Snow Leopard, but reportedly that’s not a problem, anymore). After meddling with the Javascript for a while, I settled on checking for “iPhone” in the navigator.appVersion property and adding that to the conditional wrapping the code that generates the badge link:

> if ((navigator.appVersion.indexOf(“iPhone”) == -1) && (!hasUnity || brokenUnity))

A similar test for Linux might be useful, too.