---
layout: post
title: Technical Gibberish
date: '2012-01-19T09:29:53-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515816696/technical-gibberish
---
For a while, I had some system info displayed in some of my Unity apps, partly for my own benefit and partly to assist customers in reporting useful device information (wishful thinking, perhaps). I ended up removing some of it after Amazon rejected HyperBowl initially for displaying “technical gibberish”, but it remains alive in [Fugu System](https://market.android.com/details?id=com.technicat.fugusystem)&nbsp;on Android (not on the App Store - Apple rejected it as having not enough entertainment value), which I envisioned as some hybrid between a 3D benchmarking app and one of those system info apps showing device ID’s, memory usage, etc. (never mind Unity doesn’t have all those functions). In any case, the info display code serves as an example usage of the various Unity system info functions:

`
function Start() {
guiText.text = "Device ID: "+SystemInfo.deviceUniqueIdentifier+"n"+
SystemInfo.deviceModel+"n"+
SystemInfo.operatingSystem+" "+SystemInfo.systemMemorySize + "MBn"+
SystemInfo.processorCount+" "+SystemInfo.processorType+"n"+
SystemInfo.graphicsDeviceName+" "+SystemInfo.graphicsMemorySize+"MBn"+
Screen.width+"x"+Screen.height+" pixelsn"+
"Multitouch "+(Input.multiTouchEnabled ? "yes" : "no")+
" Gyroscope "+(Input.isGyroAvailable ? "yes" : "no")+"n"+
Application.systemLanguage.ToString();
}`

