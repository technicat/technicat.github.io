---
layout: post
title: Getting Used to Xcode 5
date: '2013-10-18T21:19:23-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612503661/getting-used-to-xcode-5
---
Since I use Unity for iOS dev, I don’t need to spend much time in Xcode, but there were still enough changes in Xcode 5 to cause a bit of confusion when it came to making distribution builds. At first, I couldn’t find where to change the provisioning profile for release builds. After a brief panic, selecting All and Levels, instead of Basic and Combined, gave me what I was used to seeing in the Build Settings. The other quirk is that performing the Build then complains that it can’t find a matching provisioning profile for my attached iOS device. The workaround is to just disconnect the device before performing the Build.

[![Screen Shot 2013-10-19 at 7.41.12 AM](http://itshardtofondlepenguins.com/wp-content/uploads/2013/10/Screen-Shot-2013-10-19-at-7.41.12-AM.png)](http://itshardtofondlepenguins.com/wp-content/uploads/2013/10/Screen-Shot-2013-10-19-at-7.41.12-AM.png)

