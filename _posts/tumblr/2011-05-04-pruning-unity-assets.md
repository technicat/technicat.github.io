---
layout: post
title: Pruning Unity Assets
date: '2011-05-04T13:41:23-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412031606/pruning-unity-assets
---
I decided to perform some long-overdue housecleaning on the [HyperBowl](http://hyperbowl3d.com/) assets today. When I first started porting HyperBowl to Unity, I copied all the textures and sounds that looked like they might be used, but only a portion of them really are. This takes up unnecessary on my dev machine, especially when I copy branches of the project for other platforms (webplayer, iOS, Android…) and extra work if when I make platform-specific adjustments to the assets (e.g. I compress all audio files for webplayers, but not other platforms).

There is no convenient indication in the Unity Editor about what assets are used, but short of inspecting all the gameobjects in every scene or writing a fancy Editor script, you can check after the fact when performing a build, by inspecting the Unity Editor log file. First bring up Console from the Unity Window menu:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-04-at-10.36.17-AM.png "Screen shot 2011-05-04 at 10.36.17 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-04-at-10.36.17-AM.png)

Then click on Open Editor Log:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-04-at-10.36.58-AM.png "Screen shot 2011-05-04 at 10.36.58 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-04-at-10.36.58-AM.png)

The log will list the assets included in the most recent build:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-04-at-10.23.38-AM.png "Screen shot 2011-05-04 at 10.23.38 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-04-at-10.23.38-AM.png)

