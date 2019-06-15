---
layout: post
title: Mobile Shadows
date: '2012-08-31T21:07:20-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612435611/mobile-shadows
---
My first batch of updates built with the Unity 4 public beta is out now, and one of the new features I went nutty with is mobile dynamic shadows, as shown below in [HyperBowl High Seas](http://itunes.apple.com/us/app/hyperbowl-high-seas/id376613860). It works the same as the desktop dynamic shadows, but with some additional limitations. Only hard shadows are supported, the resolution is limited so to avoid jagged shadows you need to limit the shadow distance, which can then create the issue of shadows popping on unexpectedly as you move around (an issue I have with the shadows on the bowling pins - I just hope no one notices). For most of the [HyperBowl](http://hyperbowl3d.com/) lanes so far, I have to keep the shadow distance to no more than 30.

The other issue is performance - on the iPad2 and iPad3 (and I’m going to guess the iPhone 4S), it knocks the frame rate in HyperBowl from 60 to 30fps, and in older devices down to less than 30fps. I’m a bit leery of its performance with the retina display resolution of the iPad 3. I thought I had it looking good (screenshot below), but the released app showed some jaggy shadow edges and was oddly jittery, pausing every half second or so. But my test runs on the next update look OK. So I’ll probably turn it off again and make it a user option for now. However, for simpler apps like [Fugu Bowl](http://itunes.apple.com/us/app/fugubowl/id297032758) and [Fugu Tilt](http://itunes.apple.com/us/app/fugutilt/id295241739) I may leave it on (I should really do some profiling). And I’d love to add shadows to [Fugu Maze](http://itunes.apple.com/app/fugu-maze/id295808255).

On Android I’m leaving shadows alone. It requires depth texture support, which rules out all of my test devices (Tegra, old PowerVR…) So, at first I was wildly excited about mobile dynamic shadows and declared it my favorite feature of Unity 4, but I’ll have to back off that a bit. Still cool, but the other dynamic feature, dynamic fonts, is actually a lot more useful (now I can fix all the tiny text on the iPad 3).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/08/IMG_0016-768x1024.png "IMG\_0016")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/08/IMG_0016.png)

