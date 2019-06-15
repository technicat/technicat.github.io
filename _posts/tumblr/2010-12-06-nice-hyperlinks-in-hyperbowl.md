---
layout: post
title: Nice Hyperlinks in HyperBowl
date: '2010-12-06T22:54:56-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411990166/nice-hyperlinks-in-hyperbowl
---
The Unity [OpenURL](http://unity3d.com/support/documentation/ScriptReference/Application.OpenURL.html) function unfortunately doesn’t accept a target parameter like the [GetURL](http://www.adobe.com/support/flash/action_scripts/actionscript_dictionary/actionscript_dictionary377.html) function in Flash, so in a Unity web player, the new web page clobbers your game, and if it’s running in a frame, for example as a Facebook app, you get the awkward entire-web-page-in-someone-else’s-web-page situation.

However, the last time I complained about this (while getting [HyperBowl to run on dimeRocker Arcade](http://apps.facebook.com/dimerocker/play/hyperbowl)), Matthew Miner of dimeRocker pointed out a simple workaround by invoking Javascript in the browser using the Unity function [ExternalEval](http://unity3d.com/support/documentation/ScriptReference/Application.ExternalEval.html). You only want to use this in a web player, so I have a little wrapper for my own purposes. I might add a UNITY\_IPHONE case that brings up a web view instead of launching mobile safari, using one of the [Prime31](http://prime31.com/) plugins.  
`
static function OpenWebPage(desturl:String) {
#if !UNITY_WEBPLAYER
Application.OpenURL(desturl);
#endif
#if UNITY_WEBPLAYER
Application.ExternalEval("window.open('"+desturl+"');");
#endif
}`

