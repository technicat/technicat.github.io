---
layout: post
title: Making a HUD Camera
date: '2011-09-11T14:31:46-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515748346/making-a-hud-camera
---
I was creating a new camera for use with EZGUI, and as usual, it took me a while to remember everything I needed to set up a camera for use in HUD/GUI rendering. So I went back to [HyperBowl](http://hyperbowl3d.com/) and checked what I had there. HyperBowl in fact has two HUD cameras, one orthographic camera for relatively static elements and one perspective camera for elements that animate back and forth (like the scoreboard). Here’s the orthographic camera. The key aspects for a HUD camera are:

1. the depth is greater than (in front of) the scene camera (here I have the scene camera at depth 0, the perspective camera at depth 1, and the orthographic camera at depth 2),
2. the culling mask is set to render only the HUD elements (here we have a HUDOrtho layer for the ortho camera and a HUD layer for the perspective HUD camera)
3. &nbsp;clears depth only (of course you don’t want to clear everything drawn under it, and you have to clear the depth buffer if you don’t want your HUD disappearing into walls).
4. Usually your HUD elements are pretty close to your HUD camera, so you might as well adjust the far clipping plane accordingly.
[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/09/Screen-shot-2011-09-11-at-11.20.44-AM.png "Screen shot 2011-09-11 at 11.20.44 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/09/Screen-shot-2011-09-11-at-11.20.44-AM.png)
