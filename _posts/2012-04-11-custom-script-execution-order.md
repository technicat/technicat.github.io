---
layout: post
title: Custom Script Execution Order
date: '2012-04-11T13:43:02-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515846546/custom-script-execution-order
---
Game scripting systems usually provide Update callbacks that execute once per frame. But sometimes you want to execute some code after one or more objects have been updated, e.g. I want to update the ball-following camera in [HyperBowl](http://hyperbowl3d.com/) after the ball’s position has been updated. So Unity has a typical hack, a LateUpdate callback that runs after all Update’s have been run, and I use LateUpdate instead of Update in the camera code.

But now I have another camera script that ensures the camera doesn’t dip below the ground, and that needs to run after the follow code. I don’t expect Unity to supply a LaterUpdate callback or LateLateUpdate, but they have something better. If you select a script in the Project pane, the Inspector will present an option to customize script order:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/04/Screen-shot-2012-04-10-at-11.19.19-AM.png "Screen shot 2012-04-10 at 11.19.19 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/04/Screen-shot-2012-04-10-at-11.19.19-AM.png)

Once you click on that, you select and order scripts before and after the default. For example, I specify that my follow camera script runs after other scripts, and then I specify the ground hugging script executes after the follow script. And I just use Update, no more LateUpdate’s.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/04/Screen-shot-2012-04-10-at-12.19.48-AM.png "Screen shot 2012-04-10 at 12.19.48 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/04/Screen-shot-2012-04-10-at-12.19.48-AM.png)

