---
layout: post
title: Scaling UnityGUI
date: '2012-11-03T21:24:27-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612450481/scaling-unitygui
---
I’m fixing up some UnityGUI scripts so that they scale with the screen resolution, which isn’t as sharp as having multiple skins for various resolutions (like GUIKit001), but it’s better than nothing. Here’s the code, calculating the scaling factor and setting it in GUI.matrix. With screen dimensions, make sure you’re not dividing ints by ints!

`var baseScreenWidth:float = 320.0; // for iOS, the screen width we think we're rendering on`

function OnGUI() {  
#if UNITY\_IPHONE  
 var guiScale = Screen.width/baseScreenWidth;  
 GUI.matrix = Matrix4x4.TRS (Vector3.zero, Quaternion.identity, Vector3(guiScale, guiScale, 1));  
#endif

