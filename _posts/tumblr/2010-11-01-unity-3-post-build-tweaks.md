---
layout: post
title: Unity 3 Post-Build Tweaks
date: '2010-11-01T02:57:24-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411977716/unity-3-post-build-tweaks
---
Unity 3 covers a lot more of the iPhone build options in its Player Settings (it’s a constant game of catchup as new iOS’s appear), but I still need to make some tweaks in XCode after every Unity build.

In AppController.mm, I reduce the accelerometer sampling rate, to zero if I’m not using the accelerometer at all, or to 10 if I’m just detecting shakes. And although the Unity doc says you should just set the target frame rate to your, er, target frame rate, word on the street is you get better performance by setting it higher. And what the heck, if it actually runs at 60fps, I don’t mind.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/10/Screen-shot-2010-10-31-at-5.25.53-PM.png "Screen shot 2010-10-31 at 5.25.53 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/10/Screen-shot-2010-10-31-at-5.25.53-PM.png)

AppController.mm changes just have to be made once, as long as all the ensuing builds are Append builds (instead of Replace). In contrast, changes to info.plist are painful because each Unity build clobbers them. But there’s one setting I feel compelled to add out of conservatism - UIApplicationExitsOnSuspend allows you to specify the app will close when you hit the Home button, i.e. pre-iOS4 behavior.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/10/Screen-shot-2010-10-31-at-6.30.22-PM.png "Screen shot 2010-10-31 at 6.30.22 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/10/Screen-shot-2010-10-31-at-6.30.22-PM.png)

