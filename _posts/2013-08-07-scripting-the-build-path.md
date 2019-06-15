---
layout: post
title: Scripting the Build Path
date: '2013-08-07T13:28:16-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612494011/scripting-the-build-path
---
Here’s an extra function I added to Unity Editor script for my [HyperBowl](http://hyperbowl3d.com/) configuration menu to make sure I build to the same filename each time, located under the project folder next to Assets. Sometimes that’s not important, but sometimes it is, like when I’m updating a webplayer or executable that I’m referencing by filename. Besides, it saves a little bit of typing at build time!

    static void SetBuildPath(BuildTarget target, string name) { string path = Application.dataPath; path = path.Substring(0, path.LastIndexOf("Assets")); EditorUserBuildSettings.SetBuildLocation(target,path+"/"+name); }

and then I call it like this:

    [MenuItem ("FuguGames/HyperBowl/iOS/HyperBowl Classic")] static void Classic() { PlayerSettings.productName = "HyperBowl Classic"; PlayerSettings.bundleIdentifier = "com.technicat.HyperBowlClassic"; PlayerSettings.use32BitDisplayBuffer = true; PlayerSettings.SetScriptingDefineSymbolsForGroup(BuildTargetGroup.iPhone,"HYPERCLASSIC;"+freeDefs); iOSIcon ("classic512.png"); SetBuildPath(BuildTarget.iPhone,"iOSClassic"); TargetiOS(); }

