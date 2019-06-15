---
layout: post
title: The Profiler
date: '2009-07-19T04:13:49-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318365916/the-profiler
---
I’m an old-fashioned programmer - just give me a compiler and some variant of Emacs and I’m all set. Those newfangled IDE’s, wizards and assistants just try to turn programming into programming-for-dummies, which is fine until you really have to figure out what’s going on. I’ve never even used debuggers much - a few print statements and actually reading and thinking about your code can unravel most mysteries.

But I love profilers. Especially in Lisp and Java, call chain profilers that display a directed graph of the calls. In games that’s somewhat problematic, as a lot of time goes into “other”, but on the other hand, you have a hard target - a desired frame rate. On the first game I professionally worked on, one of the first things I did was add an fps counter. After all, how can you improve the frame rate if you can’t measure it? That’s pretty much standard now - in [Unity](http://unity3d.com/), it’s easy to add your own in a script, and the Unity Editor displays frame rate and other stats that help you discern what’s bogging down the frame rate. And I belatedly discovered the profiler on Unity iPhone that runs while you’re testing on the device (how long has that been there?)

For example this profile on an app I recently submitted to the App Store indicates I shouldn’t waste effort on optimizing my scripts - I really need to reduce the rendering burden.

![profiler](http://itshardtofondlepenguins.com/wp-content/uploads/2009/07/profiler.png "profiler")

Remember that TV show The Profiler? What if it was about a programmer optimizing code. Sixty minutes of a programmer peering at…never mind. Worst..show…ever.

But profiling is one of those programming “best practices” that can be applied universally (like in business, management and politics). Optimizing this and that might make you feel good, but in the big picture it’s useless if you don’t figure out the bottleneck and tackle that.

