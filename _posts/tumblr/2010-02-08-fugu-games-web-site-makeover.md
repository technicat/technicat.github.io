---
layout: post
title: Fugu Games web site makeover
date: '2010-02-08T15:05:47-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318421651/fugu-games-web-site-makeover
---
I took a break from [HyperBowl](http://hyperbowl3d.com/) this weekend to give the long-neglected [Fugu Games](http://fugugames.com/) web site a makeover. It has long suffered as the repository for throwing in anything I thought looked cool. That’s sort of its mission statement, but as with household cleaning, sometimes stuff has to go.

So I finally retired my early attempts at Java web games (just a couple of board games attempting to demonstrate a fairly complicated framework that could alternately target Swing and J2ME), a little Flash 3D (Papervision3d) demo, etc. The remainder now fits on one page, which allows me to use the same CSS trick I used on the HyperBowl site to present a more compact view on the iPhone web browser.

Finally, I went back to starting off the page with a Unity web player that acts as a menu for loading the other web players via the [WWW.LoadUnityWeb](http://WWW.LoadUnityWeb) function. I had a simple one with GUITextures back when I started using Unity and then abandoned it when LoadUnityWeb broke in Unity 2.0. I swore off using it, even though reportedly it’d been fixed, but sometimes there’s just one right function for the job, so I put together a new one (having lost the old one). This one is a bit more fun - the “menu” items are little 3D fugu balls that look at the mouse cursor as you move it around and swell up a bit as their mouseover behavior. I’d also like to add a mouseover sound like “click me!”, and it could use a load progress indicator (I think I’ll have the selected fugu ball swell up to fill the screen - stay tuned). Oh yeah, and I’ll have to fix all the web players that get loaded - it’s amazing (not in a good way) how software just stops working after a while.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-2.png "Picture 2")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-2.png)

