---
layout: post
title: FuguTilt 1.1 on the App Store
date: '2009-07-18T03:16:56-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318365441/fugutilt-11-on-the-app-store
---
FuguTilt was my first attempt on the iPhone, and I haven’t bothered to update it since, as can be seen from the download graph:

![Picture 31](http://itshardtofondlepenguins.com/wp-content/uploads/2009/07/Picture-31-300x278.png "Picture 31")

but with the iPhone OS 3.0 release I felt compelled to update all my apps.

[![Picture 30](http://itshardtofondlepenguins.com/wp-content/uploads/2009/07/Picture-30.png "Picture 30")](http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=295241739&mt=8)

The original version was built on the Indie version of the first Unity iPhone engine release, so this update benefits from the upgrade to Unity iPhone Pro, which drastically reduces the code size, and more incremental performance improvements stemming from the Unity maintenance releases.

Oh yeah, and I fixed an egregious physics set error&nbsp; - for you game developers out there, I failed to specify that the tilting plane was a kinematic rigidbody, meaning it has physics collision behavior but is moving under program control, not simulated physics control (like response to gravity). The result of my omission was a susceptability to balls falling through the plane instead of bouncing off it (I have to make that fix to the widget and web player version, too). It’s all in the PhysX doc you can download from nVidia.

Finally, I made some real game changes (I’m a game changer, get it?) One minor change - threw in a medium bouncy ball, augmenting the bounceless thudding ball and the ultra-springy ball that behaves like it’s filled with helium. (I’m a bit concerned that I put a point light inside each of those - that could be a real performance killer - but it seems OK so far). That one’s for Goldilocks. And I replaced the tilt control with a screen finger-swipe control for tilting the board. I’m thinking tilt controls are overrated, especially if you have to tilt the screen away from you. (And have you ever looked at your monitor or TV while plaing a game and said, wow, if I could just tilt it?) But maybe I’ll put it back in - let’s see how the swipe version does.

