---
layout: post
title: Transition Manager
date: '2011-09-28T13:08:11-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515752671/transition-manager
---
The Transitions Manager (free on the Asset Store) looks like it’ll be the latest standard component of all my Unity projects. In particular, I’m using it to add a second splash screen to my mobile apps. It’s really easy to configure - to just add a second splash screen, I use the supplied demo start scene as my initial scene, set the Next Scene to be my former initial scene, set the background color to white, specify the texture in the splash screen contents, set the number of Story images to zero (although those could be useful for adding intro instructions) and set pause detection to false. The only change I make to the script is to remove the OnApplicationPause callback.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/09/Screen-shot-2011-09-28-at-9.52.01-AM.png "Screen shot 2011-09-28 at 9.52.01 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/09/Screen-shot-2011-09-28-at-9.52.01-AM.png)
