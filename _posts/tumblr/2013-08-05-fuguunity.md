---
layout: post
title: FuguUnity
date: '2013-08-05T12:36:08-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612493606/fuguunity
---
I have some public github repos for[Unity Editor scripts](http://github.com/technicat/FuguEditor) and [scripts for iOS/Android](http://github.com/technicat/FuguMobile), but a lot of my general scripts don’t fall into those categories, so I created another repo called [FuguUnity](http://github.com/technicat/FuguUnity) (yeah, it should probably be fugu-unity, but now it would look weird since I started with the other convention). The scripts are in C# and in the Fugu namespace (Unity 3.x users will ahve to remove the declaration), and most of them so far are pretty simple (I have bunch of more complicated ones but I always have to wonder if those are too complicated…). This batching script I just drag onto the root of any hierarchy that moves together:

    public class Batch : MonoBehaviour { // Use this for initialization void Start () { StaticBatchingUtility.Combine (gameObject); } }

This one I drag onto the root of any hierarchy that should persist through scene loads:

    public class Keep : MonoBehaviour { // Use this for initialization void Start () { DontDestroyOnLoad (gameObject); } }

I call this function in the Awake/Start callback of any script that shouldn’t be used, anymore:

    public class Log : MonoBehaviour { public static void Deprecate (MonoBehaviour script) { #if FUGU\_DEBUG Debug.LogWarning("Deprecated script attached to "+script.gameObject.name); #endif } }

Finally, here’s one that’s more than a couple of lines: I drag this script onto the root of any hierarchy that should be activated/deactivated according to platform (selectable in the Inspector):

    public class PlatformActive: MonoBehaviour { public bool iOS = false; public bool Android = false; public bool webplayer = false; public bool OSX = false; public bool Windows = false; public bool Linux = false; // Use this for initialization void Awake () { #if UNITY\_IPHONE gameObject.SetActive(iOS); #endif #if UNITY\_ANDROID gameObject.SetActive(Android); #endif #if UNITY\_WEBPLAYER gameObject.SetActive(webplayer); #endif #if UNITY\_STANDALONE\_OSX gameObject.SetActive(OSX); #endif #if UNITY\_STANDALONE\_WINDOWS gameObject.SetActive(Windows); #endif #if UNITY\_STANDALONE\_LINUX gameObject.SetActive(Linux); #endif } }

