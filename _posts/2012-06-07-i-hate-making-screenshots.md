---
layout: post
title: I Hate Making Screenshots
date: '2012-06-07T15:05:34-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515866641/i-hate-making-screenshots
---
One of the surprisingly painful steps in submitting apps is making the screenshots. Even on web and desktop builds, it’s a hassle if you’re running a game that has the screen cursor locked and hidden (here it turns out a debug option that I used in my old pause menu to turn off cursor locking was unexpectedly helpful - too bad I don’t use that menu anymore).

On mobile apps, it gets worse. When I first started making iOS apps, I found the XCode screen capture feature easily enough, but figuring out where the screenshots went was another matter. Now I just take screenshots on the device, which is pretty easy if you know that it just involve pressing Power and Home simultaneously. The screenshots go into your Photo gallery and can be synced to iPhoto, but a weird problem I’ve always had that I’ve never seen anyone else mention or solve, is that oftentimes when I bring up the Choose dialog in iTunesConnect to upload screenshots, the latest ones don’t appear in the Photos folder. In those cases, if I get impatient, I end up going back to iPhoto and exporting those photos to the desktop.

But if this is a new app with iAds, it will just show test ads until the app is approved, and Apple doesn’t like to see test ads in the screenshots. So if I’ve forgotten this, I have to back, rebuild the app with ads disabled, run it on my device and take screenshots sans ads.

The Amazon appstore is the opposite. If you have ads in your app, they want to see it in the screenshot and will reject your app otherwise. (at least they did to me)

But the biggest problem by far with Android apps is the screenshot function in the Android SDK ddms tool. It (or the device) can’t handle any non-static images without shearing between frames, like this one from my [dancing skeleton app](https://play.google.com/store/apps/details?id=com.technicat.fugudance) (that leg bone is not supposed to be disintegrating):

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/06/device-2012-06-07-113403.png "device-2012-06-07-113403")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/06/device-2012-06-07-113403.png)

Did I mention I hate making screenshots?
