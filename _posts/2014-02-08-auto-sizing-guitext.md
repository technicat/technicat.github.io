---
layout: post
title: Auto-Sizing GUIText
date: '2014-02-08T04:03:32-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612522701/auto-sizing-guitext
---
I just added a couple of my GUIText utility scripts to my FuguUnity repo on github (see the lower right of this web page). One of them is not that useful, anymore, as it provides a way to select the GUIText color in the Inspector, but that’s a built-in feature, now. The other I use everywhere: a script to scale the GUIText according to screen resolution. Remember to import the font as dynamic.

    public class GUIFontSize : MonoBehaviour { public float baseHeight = 480.0f; void Start () { guiText.fontSize = (int)(guiText.fontSize \* Screen.height/baseHeight); } }
