---
layout: post
title: Unity and XCode 4
date: '2011-08-04T15:04:19-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515737886/unity-and-xcode-4
---
After the linker bug that messed up Unity apps (but only after the DRM processing that takes place after submission to the App Store), I stayed away from XCode4 for a while, but I’m back in the fold, now. Bugs aside, it’s also a pain learning new ways of doing the same things you were doing before. Here’s a quick overview of how I process Unity iOS builds, now.

I always hit the Unity Build button, not Build and Run. Partly because the Prime31 plugins work better that way, and I hear Build and Run doesn’t work with XCode4, anyway. The build is supposed to bring up XCode upon completion - that doesn’t seem to happen reliably so I double-click the resulting XCode project file. No big deal. Another inconvenience is that it always sets the target as simulator, so switch it to your test device before you start building in XCode!

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-11.23.14-PM.png "Screen shot 2011-07-27 at 11.23.14 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-11.23.14-PM.png)

The next thing I do before I build in XCode is edit the “schemes” so that my debug sessions are running with the release builds. Maybe I should run debug builds, but I figure I have to test a release build anyway before submission, so I’m willing to take this shortcut until something weird happens and I really have to debug.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-11.23.35-PM.png "Screen shot 2011-07-27 at 11.23.35 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-11.23.35-PM.png)

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-10.14.30-AM.png "Screen shot 2011-07-27 at 10.14.30 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-10.14.30-AM.png)

Finally, the last thing I change before building in XCode is to customize the source. I always set the frame rate to 60fps and lower the accelerometer sampling rate (zero if not used, 10 if I’m just checking for shakes) You would also activate the profiler at this point if you’re going to profile, but remember to deactivate it before the final build.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-10.14.01-AM.png "Screen shot 2011-07-27 at 10.14.01 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-10.14.01-AM.png)

Once I see everything’s running OK on my test devices, I change the signing identity for Release builds to my distribution identity.   
[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-12-at-1.02.14-AM.png "Screen shot 2011-07-12 at 1.02.14 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-12-at-1.02.14-AM.png)

Hit Clean, then Archive. The one thing I do like about XCode 4 is that once you archive, it brings up a validation/submission window. I’m not sure what’s the point of the validation option - I’ve successfully validated builds that I improperly signed - but the submission option saves a trip to the external Application Loader.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-10.47.37-AM.png "Screen shot 2011-07-27 at 10.47.37 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/08/Screen-shot-2011-07-27-at-10.47.37-AM.png)

