---
layout: post
title: Building Unity NaCl
date: '2012-02-19T19:37:53-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515829311/building-unity-nacl
---
One of the big new Unity 3.5 features is support for building a native Chrome webplayer. It takes only slightly more effort than building a regular Unity webplayer.

First, set your build target to webplayer with NaCl support selected.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-3.04.26-PM.png "Screen shot 2012-02-19 at 3.04.26 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-3.04.26-PM.png)

The build produces the regular webplayer files plus some files for NaCl.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-3.04.09-PM.png "Screen shot 2012-02-19 at 3.04.09 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-3.04.09-PM.png)

If you’re updating the build, you’ll need to manually increment the version number in the manifest.json file.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-3.03.53-PM.png "Screen shot 2012-02-19 at 3.03.53 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-3.03.53-PM.png)

Compress your build directory into a single zip file (the whole thing, not just the NaCl subdirectory). Go the [Chrome dashboard](https://chrome.google.com/webstore/developer/dashboard) (registering to upload on the Chrome webstore is easy but requires a one-time $5 payment), enter your app details and upload the zip file.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-4.30.32-PM.png "Screen shot 2012-02-19 at 4.30.32 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/02/Screen-shot-2012-02-19-at-4.30.32-PM.png)

There are some issues - Screen.lockCursor doesn’t work (same issue with the Unity Flash builds), which is problematic for mouse controls, and HyperBowl exported as Unity NaCl seems to run really slow in Chrome on MacOSX, slower than the regular webplayer (which defeats the purpose of NaCl!) But it runs well in Windows - [check it out](https://chrome.google.com/webstore/detail/mkhobpkhmhhpilfbnpkkkgaijfohahcf/details)!

