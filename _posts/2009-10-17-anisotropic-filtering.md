---
layout: post
title: Anisotropic Filtering
date: '2009-10-17T22:10:48-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318396011/anisotropic-filtering
---
Darn, I realized after updating the [HyperBowl Classic widget](http://www.apple.com/downloads/dashboard/games/hyperbowlclassic.html) that my latest reimport of the assets clobbered the texture [anisotropic filtering](http://en.wikipedia.org/wiki/Anisotropic_filtering) settings, which improves the appearance of textures viewed at sharp angles (instead of head-on). It makes a big difference - I fixed it in the [web player](http://hyperbowl3d.com/), so you can see the difference between the two. Here’s the web player:

[![Picture 13](http://itshardtofondlepenguins.com/wp-content/uploads/2009/10/Picture-13.png "Picture 13")](http://hyperbowl3d.com/)

The rings look pretty smooth, eh? Now take a look at the the widget:

[![Picture 14](http://itshardtofondlepenguins.com/wp-content/uploads/2009/10/Picture-14.png "Picture 14")](//www.apple.com/downloads/dashboard/games/hyperbowlclassic.html)

Notice there’s more blurring and blotchiness in the wood texture of the rings, and it’s even more distracting when you see it in motion, giving a rippling effect (oh, well, next update…) The iPhone apparently doesn’t support anisotropic filtering (or at least not much), so this artifact is also visible in the [iPhone version](http://itunes.com/app/hyperbowlclassic).

