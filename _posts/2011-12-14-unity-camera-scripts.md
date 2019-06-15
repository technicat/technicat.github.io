---
layout: post
title: Unity Camera Scripts
date: '2011-12-14T13:52:32-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515799631/unity-camera-scripts
---
Programming game cameras is a field unto itself (just check all the Game Gems articles on the subject), but Unity comes with a few camera scripts that should satisfy most of your basic needs. To get them, import the Scripts assets, which will give you a mouse orbit camera script, a smooth follow script and a smooth look-at script. Also, the Character Controller assets includes some camera scripts for first-person and third-person views.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/12/Screen-shot-2011-12-14-at-1.47.25-AM.png "Screen shot 2011-12-14 at 1.47.25 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/12/Screen-shot-2011-12-14-at-1.47.25-AM.png)

This is actually the best way to get started when you’re getting acquainted with Unity: in an empty scene, create a cube, for example, drag the mouse-orbit script to the Main Camera, set the target in the script to the cube, hit Play, and voila! A simple model viewer. The camera scripts are also a good starting point to learn scripting. Inspect the smooth look-at script, which is the simplest - this gives you an example of where the standard callbacks like Update/LateUpdate fit in, how to manipulate transforms, how to use quaternions…for each callback and function read the explanation in the Unity Scripting Reference (always do that before you start asking for free help on the forums!), then start tweaking it and see what happens!

