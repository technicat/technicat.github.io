---
layout: post
title: Always Profile
date: '2011-01-25T13:08:00-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412004671/always-profile
---
Ten years ago, this month, I had just joined the HyperBowl team and one of the first things I did was add an on-screen frame rate display. Now, with HyperBowl running on Unity, frame rate and other goodness is conveniently featured in the IDE:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/01/Screen-shot-2011-01-25-at-9.43.24-AM.png "Screen shot 2011-01-25 at 9.43.24 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/01/Screen-shot-2011-01-25-at-9.43.24-AM.png)

That tells you how what’s happening, but if you want to know why, the really cool part is the profiler.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/01/Screen-shot-2011-01-24-at-8.49.17-PM.png "Screen shot 2011-01-24 at 8.49.17 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/01/Screen-shot-2011-01-24-at-8.49.17-PM.png)

I recently noticed a frame rate drop in the Classic lane, from above 50fps to under 40fps, and wondered what had changed. A few seconds in the profiler showed me that half the CPU time was taken by water code, and I realized that somehow my script that was culling the water at a certain distance had been turned off. Clicked on the checkbox and everything’s fine again. The profiler can save you a lot of speculation.

