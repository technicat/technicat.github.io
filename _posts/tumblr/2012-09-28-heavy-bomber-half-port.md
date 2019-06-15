---
layout: post
title: Heavy Bomber Half Port
date: '2012-09-28T03:31:24-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612445456/heavy-bomber-half-port
---
I have a lot of half-completed projects, where by half I mean anywhere from ten percent to ninety percent, where that last ten percent might actually be ninety. Here’s a screenshot of one of the better-looking ones - the folks at [Heavy Water](http://heavyh2o.com/) let me try an Android port of one of their web demos, called Heavy Bomber. It’s a good example of how you can’t assume anything will just run on mobile, even a Unity web player. And it’s a good example of how you can’t make assumptions about bottlenecks. It’s got long load times due to a lot of textures, so I assumed that was the dragging down the frame rate, too. But after profiling, I realized it’s actually physics - the game is moving the level while the camera remains in a fixed position, so just moving all those colliders was dragging down the frame rate on my test phone to 5fps. Moving the camera while keeping the level fixed improves the frame rate to 25-30fps! But of course that broke the player controls. So it’s still half-complete.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/09/device-2012-09-17-155843.png "device-2012-09-17-155843")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/09/device-2012-09-17-155843.png)

