---
layout: post
title: Customizing the Unity Android Manifest
date: '2011-08-16T03:02:16-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515738986/customizing-the-unity-android-manifest
---
This wasn’t obvious to me from the documentation, but a search in the ever helpful Unity forum informed me that the Android manifest file created by Unity can be customized by placing your own version under Assets/Plugins/Android:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-08-15-at-4.07.37-PM.png "Screen shot 2011-08-15 at 4.07.37 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-08-15-at-4.07.37-PM.png)

I’m still just fumbling around with this stuff, and I don’t know what really needs to be in the manifest, so my quick and dirty technique right now is to first perform a Build, copy the manifest file from the project Temp directory to Plugins, then edit that version. Works like a charm!

