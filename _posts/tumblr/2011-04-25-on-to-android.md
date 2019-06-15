---
layout: post
title: On To Android
date: '2011-04-25T23:35:45-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412030521/on-to-android
---
I’ve been holding off on Android development because I couldn’t figure out how to use my phone for testing and the firmware I had wasn’t compatible with Unity, anyway. But I broke my phone and the warranty replacement came with upgraded firmware (Android 2.2), and I figured out where that Enable USB Debugging checkbox is in the Android settings menu, and I’m stalled on my iPhone development while Unity and Apple sort out the recent iOS 4.3 SDK issues, so I took the plunge this weekend.

First, I converted a couple of my [AppMakr](http://appmakr.com/) apps to Android. I wish there was some way I could just hit a “Make Android” button in an existing project, but I had to create new versions of each from scratch and cut-and-paste the RSS feeds into them. AppMakr seems to have a more limited feature set for Android than iOS, but still, my [Blue Mars News](https://market.android.com/details?id=com.appmakr.app175485) app is nearly identical on Android, and [La Petite Baguette](https://market.android.com/details?id=com.appmakr.app159234), rejected by Apple, is finally published, this time on the Android Market! (so there, Apple!)

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/bluenews.png "bluenews")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/bluenews.png)

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/bluepics.png "bluepics")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/bluepics.png)[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/bonappetite.png "bonappetite")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/bonappetite.png)

Self-publishing on the Android Market really feels like self-publishing - hit the Publish button, and soon after, it’s there. This made me giddy enough to cough up all the money I haven’t made on the App Store to buy a license of Unity Android Pro. I converted my [Fugu Bowl](https://market.android.com/details?id=com.technicat.FuguBowl) app easily - most of the time was spent removing the iOS plugins from [Prime31 Studios](http://prime31.com/) and figuring out the right player settings for publication.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/Screen-shot-2011-04-25-at-8.01.29-PM.png "Screen shot 2011-04-25 at 8.01.29 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/Screen-shot-2011-04-25-at-8.01.29-PM.png)

After publishing, I made an update after deciding to specify Android 2.2 as the minimum Android OS. I know this could limit my potential customer base, but I don’t want to get a bunch of customer complaints about how the app doesn’t run. I’ll probably have enough trouble anyway with all the various Android platforms I haven’t tested on. Anyway, the only thing that threw me off a bit during the update was the need to increment the Bundle Version Code.

The biggest irritation so far has been the screen capture process. There’s no hardware button combination on the phone for that, so I have to run the ddms program in the Android SDK tools directory. That worked OK for Fugu Bowl, but for [Elektra Dance](https://market.android.com/details?id=com.technicat.ElektraDance), the capture shows a lot of shearing artifacts.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/elektrascatter.png "elektrascatter")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/elektrascatter.png)

I ended up just cropping some captures from the iPhone version (the Android Market accepts several resolutions for screen captures, none of them matching the iOS resolutions).

Next, try out the AdMob and Mobclix plugins, set up merchant account for paid apps, and see what happens…

