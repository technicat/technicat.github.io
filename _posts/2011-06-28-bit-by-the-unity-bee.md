---
layout: post
title: Bit by the Unity Bee
date: '2011-06-28T13:46:34-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515727816/bit-by-the-unity-bee
---
I never quite understood Walter Brennan’s question in [To Have and Have Not](http://en.wikipedia.org/wiki/To_Have_and_Have_Not_(film)) “Have you ever been bit by a dead bee?”, but it seems to convey the feeling I get when I’ve been bitten by something not quite a bug. I just ran into one in Unity (meaning I just discovered it after letting it mess me up for a while), so here’s a list of “best practices”, or rather, bad practices to avoid:

_Overriding predefined MonoBehaviour functions._ Know your callbacks! I was wondering why some of my scene objects kept mysteriously changing position in the Editor. It’s like a form of gaslighting. Turns out I had defined some Reset functions that I call successfully at runtime to position the objects before starting an animation, but [Reset](http://unity3d.com/support/documentation/ScriptReference/MonoBehaviour.Reset.html) is a callback invoked by the Editor. Read the [Unity Scripting Reference](http://unity3d.com/support/documentation/ScriptReference/index.html)!

_Overriding Mono classes._ I think Unity warns you about this now, but at one time I implemented a class named [Dictionary](http://docs.go-mono.com/System.Collections.Generic.Dictionary%602) for a typing game (Fugu Type). That would crash the game, eventually. Since then, in lieu of namespaces, I try to ensure I pick unique names for my scripts (e.g. in HyperBowl, my classes are named HyperCamera, HyperBall, HyperTextureAnimation, etc.)

_Importing FBX at the default scale._ The default scale is 0.01, which is perfect if your model is in centimeters. When I first imported the [HyperBowl](http://hyperbowl3d.com/) assets, which were in meters, instead of reimporting with a scale of 1, I tried to adjust all the other unit-dependent parameters in the game correspondingly - near/far planes, light distances, physics settings…The result was really wonky physics. Eventually, I had to reimport everything and redo a lot of work.

_Play on Awake sounds._ When you create a new sound clip, the Play on Awake option defaults to on. That is almost never what you want, and then later when you try to figure out where that odd sound effect is coming from when you start the scene, it’s really hard to find. Save yourself some grief and turn that option off immediately.

_Don’t move with SVN._ Unity added[support for source control systems](http://unity3d.com/support/documentation/Manual/ExternalVersionControlSystemSupport.html) like [subversion](http://subversion.tigris.org/), but that just means the Unity files are (optionally) compatible with the systems. It’s not really integrated, so if you commit your project to subversion and then move or delete some files, it’s a mess - you have to separately inform subversion that you moved/deleted them. So do your reorg first, or wait for [Unity 3.5](http://blogs.unity3d.com/2011/06/16/unity-roadmap-2011/).

