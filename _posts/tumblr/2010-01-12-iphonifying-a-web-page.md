---
layout: post
title: iPhonifying a Web Page
date: '2010-01-12T14:35:29-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318414361/iphonifying-a-web-page
---
Safari on the iPhone does a pretty good job of viewing regular web pages, but the browsing experience can be vastly improved by tailoring a page for the iPhone (compare the Mobile vs. Standard view of the Twitter site on the iPhone).

This is particularly true for the [HyperBowl](http://hyperbowl3d.com/) page, which replicates the 800x600 PC game, and moreover displays additional product information to the right.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/Picture-7.png "Picture 7")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/Picture-7.png)

First, I added a style sheet that only loads when browsing from the iPhone. This style sheet contains settings that overrides the original.

Then I specify the viewport width is the width of the iPhone screen. Otherwise, we’ll start out at the default page width (960 pixels, I think) and have to zoom in to read.

And here’s the result. Not as fancy, but a lot more readable!

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/IMG_0362.png "IMG\_0362")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/IMG_0362.png)

