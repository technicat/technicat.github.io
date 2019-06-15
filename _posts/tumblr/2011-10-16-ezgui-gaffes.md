---
layout: post
title: EZGUI Gaffes
date: '2011-10-16T02:14:13-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515782796/ezgui-gaffes
---
After an interlude of a few weeks, I returned to EZGUI to add a pause menu to another app, [Fugu Match](https://market.android.com/details?id=com.technicat.fugumatch), and repeated a bunch of mistakes I made the first time around, so it’s probably time to start listing them for future reference.

One problem I ran into first time around is that I didn’t have a proper width and height set for my buttons, which made it really hard to click/tap on them:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-5.29.18-PM.png "Screen shot 2011-10-15 at 5.29.18 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-5.29.18-PM.png)

Another issue, when setting changing fonts, you need to specify both the font text file and the font material - you’ll get bizarre results if they don’t match. It’s easy to miss the material on sprite text objects - for those, the font material is in the mesh renderer.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-5.33.09-PM.png "Screen shot 2011-10-15 at 5.33.09 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-5.33.09-PM.png)

Back to the button, don’t overlook the whenToInvoke property. I prefer PRESS for a snappy response, but that’s not the default. And make sure the panel manager property is properly set (if the button is in a panel).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-12.35.42-PM.png "Screen shot 2011-10-15 at 12.35.42 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-12.35.42-PM.png)

And the one that really messed me up each time - make sure you have your UI layer specified in all the right places, i.e. all the UI objects, in the culling mask for your UI camera, and in the UI manager list of UI cameras (I kept forgetting that last one).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-5.28.09-PM.png "Screen shot 2011-10-15 at 5.28.09 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/10/Screen-shot-2011-10-15-at-5.28.09-PM.png)

