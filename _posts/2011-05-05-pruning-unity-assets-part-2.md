---
layout: post
title: Pruning Unity Assets, Part 2
date: '2011-05-05T15:04:49-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412032051/pruning-unity-assets-part-2
---
Just a followup on yesterday’s blog on checking the Unity build log to see which assets you’re really using. The build log lists assets in descending order of file size, which is great when you’re optimizing the build size and not so great when you want to compare the list with what you’ve got in your Unit project directory. However, the Mac Console has a convenient text search box that shows filtered results, so if you arrange your assets in appropriate directories (putting them all in one top-level directory is not going to help you), you can simplify the comparison. For example, I placed all the sounds that can be used for the [HyperBowl](http://hyperbowl3d.com/) bowling ball in the directory Sounds/Ball, so after a build, I can select Unity Editor.log file in the Console, type “Sounds/Ball” in the Console search field, and here it lists what is actually used from that directory in my Unity Assets folder.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-05-at-11.56.43-AM.png "Screen shot 2011-05-05 at 11.56.43 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-05-at-11.56.43-AM.png)

