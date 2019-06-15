---
layout: post
title: Logging with Unity Android
date: '2011-05-24T13:58:31-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412036096/logging-with-unity-android
---
Logging a test run with Unity Android is not difficult, but the steps are different than with Unity iOS.

First, if you want to see profiling information in your log, check that option in your Player Settings:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-24-at-10.34.08-AM.png "Screen shot 2011-05-24 at 10.34.08 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-24-at-10.34.08-AM.png)

Then, when you build, make sure Development Build is selected in your Build Settings:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-24-at-10.34.55-AM.png "Screen shot 2011-05-24 at 10.34.55 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/05/Screen-shot-2011-05-24-at-10.34.55-AM.png)

Before you run, start up logcat with a filter so you only see Unity messages:

./adb logcat Unity:V \*:S

Then when you run, you should see debug messages (including your own Debug.Log calls)

——— beginning of /dev/log/main  
——— beginning of /dev/log/system  
D/Unity&nbsp;&nbsp; (22494): Creating OpenGL ES 2.0 context (RGB16 565 24/8)  
D/Unity&nbsp;&nbsp; (22494): Creating OpenGL ES 2.0 context (RGB16 565 24/8)

and profiling info if you selected that option:

D/Unity&nbsp;&nbsp; (22782): —————————————-  
D/Unity&nbsp;&nbsp; (22782): Android Unity internal profiler stats:  
D/Unity&nbsp;&nbsp; (22782): cpu-player\>&nbsp;&nbsp;&nbsp; min:&nbsp; 1.8&nbsp;&nbsp; max: 10.1&nbsp;&nbsp; avg:&nbsp; 4.2  
D/Unity&nbsp;&nbsp; (22782): cpu-ogles-drv\> min:&nbsp; 0.7&nbsp;&nbsp; max:&nbsp; 2.4&nbsp;&nbsp; avg:&nbsp; 0.9  
D/Unity&nbsp;&nbsp; (22782): cpu-present\>&nbsp;&nbsp; min:&nbsp; 8.0&nbsp;&nbsp; max: 15.7&nbsp;&nbsp; avg: 13.0  
D/Unity&nbsp;&nbsp; (22782): frametime\>&nbsp;&nbsp;&nbsp;&nbsp; min: 13.1&nbsp;&nbsp; max: 24.0&nbsp;&nbsp; avg: 18.1  
D/Unity&nbsp;&nbsp; (22782): draw-call #\>&nbsp;&nbsp; min:&nbsp; 14&nbsp;&nbsp;&nbsp; max:&nbsp; 14&nbsp;&nbsp;&nbsp; avg:&nbsp; 14&nbsp;&nbsp;&nbsp;&nbsp; | batched:&nbsp;&nbsp;&nbsp; 14  
D/Unity&nbsp;&nbsp; (22782): tris #\>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; min: 11375&nbsp; max: 11375&nbsp; avg: 11375&nbsp;&nbsp; | batched:&nbsp; 5564  
D/Unity&nbsp;&nbsp; (22782): verts #\>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; min:&nbsp; 8519&nbsp; max:&nbsp; 8519&nbsp; avg:&nbsp; 8519&nbsp;&nbsp; | batched:&nbsp; 3579  
D/Unity&nbsp;&nbsp; (22782): player-detail\> physx:&nbsp; 0.1 animation:&nbsp; 0.0 culling&nbsp; 0.0 skinning:&nbsp; 0.0 batching:&nbsp; 0.1 render:&nbsp; 3.0 fixed-update-count: 0 .. 1  
D/Unity&nbsp;&nbsp; (22782): mono-scripts\>&nbsp; update:&nbsp; 0.5&nbsp;&nbsp; fixedUpdate:&nbsp; 0.0 coroutines:&nbsp; 0.0  
D/Unity&nbsp;&nbsp; (22782): mono-memory\>&nbsp;&nbsp; used heap: 684032 allocated heap: 1183744&nbsp; max number of collections: 0 collection total duration:&nbsp; 0.0

