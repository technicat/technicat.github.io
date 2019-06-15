---
layout: post
title: Fat-Free Flares
date: '2011-03-05T19:05:03-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412013266/fat-free-flares
---
Lens flare effects are a bit gimmicky - they mimic a lens artifact you would never actually see in real life unless you walk around looking through a camera, but they look cool, and to be fair, we’re mimicking a cinematography gimmick.

To make matters worse, sometimes I want to see a lens flare without actually having a light as the source. This is for performance reasons - to see the lens flare I need to put the light in a place that doesn’t actually light up the areas I want lit, so it’s an extra expense I don’t need, particularly on the iPhone, as with [Fugu Bowl](http://itunes.apple.com/us/app/fugubowl/id297032758?mt=8).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-04-at-9.24.15-AM.png "Screen shot 2011-03-04 at 9.24.15 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-04-at-9.24.15-AM.png)

This is my typical cheat - I assign the flare to a directional light, but then set the light culling mask to no layers.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-04-at-9.24.00-AM.png "Screen shot 2011-03-04 at 9.24.00 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-04-at-9.24.00-AM.png)

Actually, it’s probably better to just make a game object and attach a Flare component, which gives you the most flexibility. In any case, the real expense can be the flare itself, depending which one you choose (besides the ones that come standard with Unity, check out the Lens Flare package on the Asset Store). Some of the more magnificent flares can drop your frame rate from 30fps to 20fps easily (with more impact on the Retina and iPad displays, due to the pixel count).

