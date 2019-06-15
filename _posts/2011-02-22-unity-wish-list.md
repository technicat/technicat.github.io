---
layout: post
title: Unity Wish List
date: '2011-02-22T14:47:09-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412009951/unity-wish-list
---
Christmas is past, but anyway, here’s my Unity wish list (by the way, I’ve spent $4000 on Unity licenses, so everyone complaining about how their Indie licenses don’t include Pro features, get back in line).

- Less reliance on FBX. I know it has to be supported, but relying on the FBX SDK to handle OBJ and Collada imports (never see that officially confirmed, but I think that’s what’s happening) is asking for trouble.
- Remove that default .01 scaling factor on FBX imports, or at least allow setting a new default. Importing generally works pretty well, but the automatic import is pretty useless if I have to manually adjust and reimport everything. And it really messed me up when I didn’t realize the default scaling factor was not 1 - I ended up blaming artists (more enjoyable when I’m right) and scaling the physics system (doesn’t scale well by two orders of magnitude).
- Per-platform audio import settings. Just like the per-platform overrides on texture imports. I definitely want to compress all audio on my web players, but not necessarily on desktop or iOS builds.
- Player settings to customize the About box on desktop builds.
- Player settings that fill out the required info.plist entries for Mac App Store builds (life is too short to spend filling out info.plist files)
- A checkbox on iOS builds for UIApplicationQuitsOnSuspend. Not really that important, but there are some apps where I feel it makes more sense for them to restart when you exit and resume.
- Create game objects underneath a selected object. At least half the time, when I create a game object I want it somewhere within a hierarchy, and it’s a hassle to create, find and drag it back to the desired spot, especially in complex scenes.
- Application.OpenURL should have a target parameter like the Flash equivalent. In web players, I almost never want to clobber the current page with the new one.
- A UNITY\_PRO compiler define so scripts can be shared among Pro and Indie.
- Fix the forums! I can’t unsubscribe from threads, and I often miss emails from those threads that I do want to remain subscribed to.
- Remove the feature request feature from the bug reporter, or link it to the feedback site. Unity seems to want everyone to use the [feedback site](http://feedback.unity3d.com/) instead, but as long as it’s there, it’s not clear whether we’re supposed to submit feature requests to one or both.
- More allowed votes on the feedback site. Only ten are allotted, which means you can only submit ten feature requests, and if you do, then you can’t vote up anyone other requests. You can easily get around that by creating multiple logins (I accidentally created a second one when I forgot about my first&nbsp; one, which I’d stopped using because I ran out of votes), but then, that just seems silly.
- Oh, almost forgot this one - scale down the Magic Mouse Input.GetAxis values. It really messes up [HyperBowl](http://hyperbowl3d.com/) and you can notice it makes Unity mouse-look (including first person controllers) way too twitchy.
