---
layout: post
title: Physics on the High Seas
date: '2010-05-29T00:04:14-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411929326/physics-on-the-high-seas
---
Each additional [HyperBowl](http://itunes.apple.com/us/app/hyperbowl/id344209253?mt=8) lane ported to the iPhone/iPad presents new challenges. With the High Seas lane (submitted to the App Store a couple of days ago - fingers crossed!), it’s physics performance. I learned two things: rigidbodies are slow, and moving mesh colliders are slow. That’s relative, of course. On my Mac and PC, a rocking ship that has a rigidbody with a mesh collider is no big deal. On my iPad, switching it to a collection of primitive colliders with no rigidbodies is the difference between 15ps and 30fps. (and on my iPod touch, it’s the difference between 5fps and 10fps, which is why this lane is iPad only).

So I spent much of the past week placing invisible box colliders around the ship, just enough to cover all the surfaces the bowling ball can hit. Less is more, and just enough is perfect.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/05/Screen-shot-2010-05-26-at-12.25.51-PM.png "Screen shot 2010-05-26 at 12.25.51 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/05/Screen-shot-2010-05-26-at-12.25.51-PM.png)

