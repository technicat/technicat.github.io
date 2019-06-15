---
layout: post
title: Building DEX Failed
date: '2012-01-27T19:39:40-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515817786/building-dex-failed
---
Unity Android users will occasionally run into a “building DEX failed” error when building, particularly with plugins. Normally, double-clicking on the error message in the bottom of the Editor will bring you to more information in the console window:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/01/Screen-shot-2012-01-23-at-10.17.49-PM1.png "Screen shot 2012-01-23 at 10.17.49 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/01/Screen-shot-2012-01-23-at-10.17.49-PM1.png)

But in this case, likely there will be a long java stacktrace that is incompletely displayed. What you need to do here is go the extra inch in debugging effort and bring up the Editor log, which will display the entire trace - you’ll want to search for the error and scroll to the bottom to see the real error, which in this example shows that I inadvertantly added the openfeint functions twice in my plugin directory (in two separate jar files). It really helps if you know Java, too - the more the better. At least understand what jar files are, and the java command-line tools like javac and jar!

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/01/Screen-shot-2012-01-23-at-10.16.32-PM.png "Screen shot 2012-01-23 at 10.16.32 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/01/Screen-shot-2012-01-23-at-10.16.32-PM.png)

