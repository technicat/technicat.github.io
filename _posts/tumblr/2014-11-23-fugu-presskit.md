---
layout: post
title: Fugu Presskit
date: '2014-11-23T22:47:35-08:00'
tags:
- presskit
tumblr_url: https://fugugames.tumblr.com/post/110698075006/fugu-presskit
---
There’s nothing like having the source code. After experimenting with using tumblr as my [Fugu Games](http://fugugames.com/) site,I went back to a standalone site, this time using [presskit](http://dopresskit.com/), becuase I wanted something where I could easily have separate pages for each app. There’s a little bit of weirdness with presskit, e.g. the code calls a ParseLink function extracts a portion of each URL for display, but then rewraps them with “http://” for href attributes, which messes up some variations of URLs. But that was an easy change to make in the script.

A bigger change I made was to add support for twitter cards. So now if someone shares one of the page URLs on twitter, the corresponding app will show up nicely (and according to the device you’re viewing it from!) Now I just need a tweet button each page…

[![IMG_0268](http://itshardtofondlepenguins.com/wp-content/uploads/2014/11/IMG_0268.png)](http://itshardtofondlepenguins.com/wp-content/uploads/2014/11/IMG_0268.png)

