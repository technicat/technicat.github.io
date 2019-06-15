---
layout: post
title: Layer-Based Collision
date: '2011-03-19T11:42:05-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412017506/layer-based-collision
---
I’m still catching up on new Unity features. One that I wish I’d used in my last [HyperBowl](http://itunes.apple.com/us/app/hyperbowl/id344209253?mt=8) update is layer-based collision, especially since I added colliders to some HUD elements so I could do raycasts for touch input (the new layer parameter for the raycasts functions are helpful, too, e.g. now the touch input code just performs raycasts on the HUD layers). Now I’m worried players may bowl into invisible mystery objects. So, the next update (already?) will have this - my only minor quibble is that it’d be nice to select/deselect a row/column at once. This was a lot of clicking.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-16-at-10.37.08-PM.png "Screen shot 2011-03-16 at 10.37.08 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/03/Screen-shot-2011-03-16-at-10.37.08-PM.png)

