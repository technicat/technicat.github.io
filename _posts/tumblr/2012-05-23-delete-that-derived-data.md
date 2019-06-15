---
layout: post
title: Delete That Derived Data
date: '2012-05-23T01:25:43-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515862311/delete-that-derived-data
---
Once in a while, I get a weird error Xcode build error saying something like something was changed after a precompiled header was generated. I used to get around it by deleting the entire project and starting again, but a search on the Unity forum turned up a better way - go to the Organizer window, select Projeccts, and remove the derived data for the project. The next build will take longer, but it will complete (unless you have some other problem). Also, you may find a while bunch of other derived data that you can delete, and that can free up a ton of disk space.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-20-at-2.52.42-PM.png "Screen shot 2012-05-20 at 2.52.42 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-20-at-2.52.42-PM.png)

