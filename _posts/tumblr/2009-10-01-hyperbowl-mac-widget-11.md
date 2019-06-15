---
layout: post
title: HyperBowl Mac Widget 1.1
date: '2009-10-01T01:08:04-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318388781/hyperbowl-mac-widget-11
---
An updated [HyperBowl Mac widget](http://www.apple.com/downloads/dashboard/games/hyperbowlclassic.html) is now on the web site - submitted it Monday, saw it there on Tuesday! (quite a difference from the App Store review time) Didn’t get Feature Widget status this time, but still a Staff Favorite and hanging in the [Top 50](http://www.apple.com/downloads/dashboard/top50/) download list. So, no complaints. This update fixes a crash/freeze that occurs if you get a spare in the ninth frame (an embarrassing code bug) and has a new trophy scene as shown below.

![Picture 1](http://itshardtofondlepenguins.com/wp-content/uploads/2009/09/Picture-11.png "Picture 1")

Under the hood, it’s a rather substantial rework - the previous version had assets imported at 1/100 of the proper scale (due to a default import scaling option in Unity), so I scaled down physics to match, which is supposed to work. But it doesn’t. When I reimported everything without the shrinkage and leaving physics parameters alone, the bowling pins behave much better. In particular, they don’t get stuck in a partial fall/roll and just stand there tilting. Plus I added a flat collider to the bottom of the pins so they can wobble a bit if they just get a glancing blow. Seems to me even the lighting works a bit better and the materials automatically pick up the right textures when I reimported (as opposed to manually attaching each one the first time I did it) Lesson learned - from now on when I’m importing assets, I’ll be sure to reimport them immediately at the desired scale. Now, anxiously awaiting the new iPhone version to show up on the App Store…

