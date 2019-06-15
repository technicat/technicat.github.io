---
layout: post
title: Ads and IFDEF's
date: '2013-07-29T05:21:52-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612492876/ads-and-ifdefs
---
For mobile ads, I started out with the prime31 iAd plugin, then switched to the Unity iAd functions, then back to the prime31 plugin, and on Android I used the prime31 AdMob plugin. Using separate scripts for each, this got kind of unwieldy and error prone configuring for different builds. But with the miracle of custom preprocessor definitions, I’m now using one script and just mess with the Player Settings for each build:

    public class AdBanner : MonoBehaviour { public bool showOnTop = true; public string AdMobID = ""; #if P31\_IAD void Start() { AdBinding.createAdBanner (!showOnTop); } #endif #if UNITY\_IPHONE && FUGU\_ADS && !P31\_IAD private ADBannerView banner = null; IEnumerator Start() { GameObject.DontDestroyOnLoad(gameObject); // keep ad alive if we load a new scene banner = new ADBannerView(); banner.autoSize = true; banner.autoPosition = showOnTop ? ADPosition.Top : ADPosition.Bottom; while (!banner.loaded && banner.error == null) { yield return null; } if (banner.error == null) { banner.Show(); } else { banner = null; } } #endif #if UNITY\_ANDROID && FUGU\_ADS void Start() { AdMobAndroid.init(AdMobID); AdMobAndroid.createBanner(AdMobAndroidAd.smartBanner, showOnTop ? AdMobAdPlacement.TopCenter : AdMobAdPlacement.BottomCenter); } #endif }

