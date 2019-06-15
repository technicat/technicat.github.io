---
layout: post
title: UnityEngine.Object
date: '2012-11-09T00:48:21-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612451781/unityengineobject
---
In the minor mystery cleared up department: for the longest while I’ve been using GameObject instead of Object to prefix static functions like DontDestroyOnLoad that are documented to be defined in Object, because I was getting compiler errors on them. Turns out in Javascript, Object resolves to System.Object from .NET instead of UnityEngine.Object from Unity. The workaround is to specify UnityEngine.Object instead of Object. Not an issue with C#, where it resolves to UnityEngine.Object.

I guess I’ve never seen this mentioned by anyone else because you rarely need to specify Object - I just happen to like typing out Object.DontDestroyOnLoad, for example, because it makes clear that it’s a static function call and spells out which class its defined in (which is handy if you’re the type that actually looks up the documentation for each function)
