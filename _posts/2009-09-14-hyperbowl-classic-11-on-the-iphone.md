---
layout: post
title: HyperBowl Classic 1.1 on the iPhone
date: '2009-09-14T00:30:53-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318383966/hyperbowl-classic-11-on-the-iphone
---
HyperBowl Classic 1.1 is now on the [App Store](http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=322930268&mt=8) after a two-week approval period (which, coincidentally?, is how long it took to get the 1.0 version approved). Waiting is always a nerve-wracking business but in the meantime I showed it to a neighbor who doesn’t even have an iPhone and he seemed delighted with it, playing the game all the way through. So I felt a little more secure. Anyway, here is the updated App Store page:

[![Picture 18](http://itshardtofondlepenguins.com/wp-content/uploads/2009/09/Picture-18.png "Picture 18")](http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=322930268&mt=8)

I see some glitchiness in the App Store links - the top link (not displayed here) displayed as “AppStore -\> Games -\> HyperBowl Classic” still points a page for the 1.0 version as of this writing, but maybe that’s one of those things that resolves itself over time (it generally takes a few hours for a newly-approved app and accompanying informational changes to fully appear on iTunes).

In any case, this update came just a bit later than I originally intended because I was waiting for the [Unity](http://unity3d.com/) iPhone 1.5 update, and it was well worth the wait.&nbsp; The engine upgrade, in particular the batching feature, and just one piece of my own custom-culling code (the water rendering is pretty expensive and not culled by another method, so I disable it until you roll past the pin area, and of course re-disable it when you roll back away) resulted in significantly improved frame rate (if you have an iPhone 3G-S, it should run great).

I also switched to the new blob shadow provided in Unity iPhone and switched the star background from a skybox to the iPhone-specific background shader (which isn’t documented, yet, but it seems like the right thing to do) Besides that, I made a few fixes that apparently no one else noticed, like some collision walls not matching the visible walls on the left and right.

A little bit reluctantly, I built the app with iPhone SDK 3.0, so now you need iPhone OS 3.0 (or 3.1) to play it. Now that I’m testing on 3.0, I can’t be 100% sure it runs on anything less (on the other hand, it’s not like I’m testing on every variation of iPod touch and iPhone hardware), and I figure, there’s no reason everyone can’t update their OS at this point. OS 3.0 is free for iPhone users, and although it’s a rip-off to charge iPod touch users, if they won’t pay $4.99 for the upgrade, chances are they’re not gonna pay $.99 for my app.

I’m trying to be conservative about adding content, since it’s pretty easy to trigger an out-of-memory crash (it may not even be your app’s fault, just run some memory hogs just before your app). But I did add a new logo scene, which is basically the original logo scene you see in the arcade/attraction version. Next update, I plan to add the original trophy scene that appears at the end of the game - if no one complains about out-of-memory crashes, that is.

