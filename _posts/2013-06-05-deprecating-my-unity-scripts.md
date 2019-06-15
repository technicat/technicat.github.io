---
layout: post
title: Deprecating My Unity Scripts
date: '2013-06-05T12:52:44-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612481641/deprecating-my-unity-scripts
---
I’m well past the point where I have old versions of functions I don’t want to use, particularly as I’m replacing JavaScript with C#, but I’m afraid to take them out because I might still be using them somewhere. Ideally, I’d have some Editor script that would root them out, but in the meantime, it’s also nice to have some kind of deprecation warning (I think I used to be able do that in some other language, maybe Common Lisp, but it’s been so long…)

So I cobbled up a really simple logging function, in a namespace/class Fugu.Log, that warns a deprecated script is in use:

`
public static void Deprecate (MonoBehaviour script) {
Debug.LogWarning("Deprecated script attached to "+script.gameObject.name);
}`

and then I put this in the Awake or Start callback of the deprecated script:

`
Fugu.Log.Deprecate(this);`

Then hit Play and check the Console. By the way, I did try adding System.ObsoleteAttribute but haven’t seen it do anything (at least in JavaScript).

