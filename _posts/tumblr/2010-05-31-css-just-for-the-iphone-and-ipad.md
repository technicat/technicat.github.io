---
layout: post
title: CSS Just for the iPhone and iPad
date: '2010-05-31T03:19:36-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411930201/css-just-for-the-iphone-and-ipad
---
The iPad is a nice web-browsing appliance, Flash aside, but I found my [HyperBowl](http://hyperbowl3d.com/) site was scrunched in it, quite possibly because I had this in the HTML header as a trick to specially format it for the iPhone:

    \<meta name="viewport" content="width=device-width"/\>

So where I had a CSS for the iPhone and another for everything else, I now have one more CSS for the iPad. The order is important.

    \<link href="hyper2.css" type="text/css" rel="stylesheet"\> \<link media="only screen and (max-device-width: 1024px)" href="hyperipad.css" type="text/css" rel="stylesheet" /\> \<link media="only screen and (max-device-width: 480px)" href="hyperiphone.css" type="text/css" rel="stylesheet" /\>

