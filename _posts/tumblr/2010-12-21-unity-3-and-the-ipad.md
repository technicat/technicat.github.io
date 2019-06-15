---
layout: post
title: Unity 3 and the iPad
date: '2010-12-21T18:09:40-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411994961/unity-3-and-the-ipad
---
This is old news by now, but I thought I’d note the changes the Unity 3 changes that affected my iPad development. Basically, there was one added convenience and one inconvenience. For the former, I no longer have to specify both landscape and portrait splash screens (you could leave one out before, but then you had to manually remove the reference to the missing image in XCode).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/12/Screen-shot-2010-12-21-at-2.05.24-PM.png "Screen shot 2010-12-21 at 2.05.24 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/12/Screen-shot-2010-12-21-at-2.05.24-PM.png)

The inconvenience was a one-time thing - some iPhoneInput properties were deprecated and moved to the new Input class, since they’re applicable to other platforms (like Android). So I updated my screen-orientation code, listed in the [iPad chapter of my Unity tutorial](http://drupal.technicat.com/games/unity/iphone/ipad.html).

