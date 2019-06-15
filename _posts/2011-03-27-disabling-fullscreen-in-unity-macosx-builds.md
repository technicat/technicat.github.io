---
layout: post
title: Disabling Fullscreen in Unity MacOSX Builds
date: '2011-03-27T17:42:41-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412019601/disabling-fullscreen-in-unity-macosx-builds
---
The latest submission of [HyperBowl](http://hyperbowl3d.com/) to the Mac App store got rejected due to a bug when switching from fullscreen to windowed mode (reportedly the cursor gets stuck in the screen corner, but I haven’t reproduced it). My expedient solution is to just remove fullscreen mode. I didn’t really like worrying about the squash and stretch issue, anyway (or so I rationalize).

Unity lacks an option to disable fullscreen, but it’s not hard to do remove it in a MacOSX build (you just have to do it after every build). Just invoke a Show Package on the app to find the MainMenu nib file:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-27-at-2.29.45-PM.png "Screen shot 2011-03-27 at 2.29.45 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-27-at-2.29.45-PM.png)

and then in XCode remove the fullscreen menu item (select, then perform a Cut in the Edit menu):

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-27-at-2.30.42-PM.png "Screen shot 2011-03-27 at 2.30.42 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-27-at-2.30.42-PM.png)

This still leaves the “Windowed” checkbox in the resolution dialog, so if you’re enabled that dialog, you’ll probably want to edit that nib file, also.

