---
layout: post
title: WordsEye Feature 1.3
date: '2009-12-04T01:11:41-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318407841/wordseye-feature-13
---
[WordsEye Feature 1.3](http://itunes.com/app/wordseyefeature) appeared on the App Store this week. It just has one fix - [WordsEye](http://wordseye.com/) scenes are now scaled to fit the iPhone screen:

![IMG_0047](http://itshardtofondlepenguins.com/wp-content/uploads/2009/12/IMG_0047.png "IMG\_0047")

In the previous version, the images were not scaled, and since they’re slightly larger than the iPhone screen a bit is cropped off the top and the right (like some of the haircuts I used to get)

![IMG_0086](http://itshardtofondlepenguins.com/wp-content/uploads/2009/12/IMG_0086.png "IMG\_0086")

Scaling-to-fit changes squashes the original image a bit, but I think it looks better overall. Of course, I could letterbox it (except the empty areas would go on the sides), but still, I think it looks better to fill up the screen.

Actually, that was the original behavior, but then (anyone not using [Unity](http://unity3d.com/) stop reading here) I realized I had a massive memory leak accessing the convenient but deadly [WWW.texture](http://WWW.texture), so then I switched to [WWW.DownloadImageToTexture](http://WWW.DownloadImageToTexture) which seemed to ignore the pixel insets that made [WWW.texture](http://WWW.texture) fit the screen (and only on the iPhone - works fine on the [widget](http://www.apple.com/downloads/dashboard/justforfun/wordseyefeature.html) version), but this time around, I belatedly realized that DownloadImageToTexture will automatically scale to the target texture, which makes sense - it’s hard to download images if you have to know their original size. So now it just downloads into a screen-sized texture instead of into a texture matching the original image size with a bunch of insets that attempt to mash it into place. So we’ve gone from broken-but-simple to broken-in-a-less drastic-way-but complicated to simple-again-and-hopefully-nothing-broken.

