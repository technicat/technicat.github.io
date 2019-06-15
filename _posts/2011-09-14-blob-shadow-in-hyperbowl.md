---
layout: post
title: Blob Shadow in HyperBowl
date: '2011-09-14T14:57:53-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515750011/blob-shadow-in-hyperbowl
---
Unity doesn’t support real shadows on mobile devices (by real, I mean shadows dynamically computed from the shadowing geometry), but you can project shadow textures onto surfaces using the Projector component. In fact, Unity includes a blob shadow prefab. Which reminds me of the time I worked on replacing the blob shadows in a skateboarding game with detailed shadows via shadow maps, only to have the game director decide the blob shadows looked better (hey, that was my job, to give him a choice!)

Anyway, that is one feature from the original [HyperBowl](http://hyperbowl3d.com/) that is missing in the new version for iOS, and I’m rectifying that by now by adding a blob ball shadow for HyperBowl on the iPad2 (on other devices, I’m on the edge with the frame rate for the bigger levels). That is one of the remaining user complaints I have to address - there has been only one, but that guy actually emailed me and left two strident reviews on the App Store. I hope he has an iPad2.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/09/IMG_0072.png "IMG\_0072")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/09/IMG_0072.png)
