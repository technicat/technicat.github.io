---
layout: post
title: Integrating Kiip
date: '2012-05-02T12:52:48-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515854626/integrating-kiip
---
The first nickel of revenue from my first integration of [Kiip Rewards](http://kiip.me/) (on [Fugu Maze](http://itunes.apple.com/app/fugu-maze/id295808255)) has rolled in, so I’m trying it out on some more apps, and of course, now I have to relearn the integration steps.

Overall, it’s pretty simple. Just go to github, search for “kiip” and you’ll find their Unity SDK, with the integration steps listed in their readme file. The core Kiip library itself is presented as a download after you create a Kiip developer account, add your app (if it’s a published app, the dashboard conveniently fills in the app information when you type in the name), and start the walkthrough.

As is often the case, the most tedious portion of the integration is in XCode. After you perform the Unity build, you need to add the Kiip library to your project:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-04-30-at-11.41.35-PM.png "Screen shot 2012-04-30 at 11.41.35 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-04-30-at-11.41.35-PM.png)

And then add the MobileCoreServices framework and libxml dylib (bottom of the Build Phases tab)

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-04-30-at-11.44.33-PM.png "Screen shot 2012-04-30 at 11.44.33 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-04-30-at-11.44.33-PM.png)

One final thing that might trip you up - in the dashboard you have to complete the walkthrough by click on the Submit button for Kiip to be activated with your app.

