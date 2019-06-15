---
layout: post
title: EasyConsole
date: '2013-06-30T19:34:22-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612484601/easyconsole
---
I started putting stuff like an FPS display option in the HyperBowl menu, largely for my own convenience, but that’s really what a console is useful for and something I miss working on console and PC games (although the original version of [HyperBowl](http://hyperbowl3d.com/)didn’t have one either - I cobbled up an FPS display then by setting it as an init file option).

So I finally checked this off my what-I-want-to-do-instead-of-what-I-should-be-doing list and picked up EasyConsole from the Asset Store. There are several console packages, but I chose EasyConsole for is NGUI interface (also has one in UnityGUI). The NGUI prefab is a little bit out of date - missing script references when I use it with my installation of NGUI, which is the latest - and there are some SetActiveRecursively warnings, so it would be nice to have that cleaned up with Unity 4 - but overall it’s pretty easy to use. I pared down the interface, changed the Update to just happen on callback, which is more efficient, particularly considering there’s some string concatenation going on there, and merged it into the HyperBowl pause menu. Now you can toggle the FPS display and obtain device and graphics hardware info. Again, that’s largely for my convenience, but who knows, maybe someone else will find it fun to play with.

[![Screen Shot 2013-06-27 at 7.59.36 PM](http://itshardtofondlepenguins.com/wp-content/uploads/2013/06/Screen-Shot-2013-06-27-at-7.59.36-PM.png)](http://itshardtofondlepenguins.com/wp-content/uploads/2013/06/Screen-Shot-2013-06-27-at-7.59.36-PM.png)

