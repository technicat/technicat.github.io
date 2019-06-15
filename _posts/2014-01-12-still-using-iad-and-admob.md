---
layout: post
title: Still Using iAd (and AdMob)
date: '2014-01-12T07:43:06-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612514891/still-using-iad-and-admob
---
Despite my rant a while back that I was dropping iAd because they turned off my revenue without telling me that my iAd contract was (incorrectly) terminated, I’m still using it. Sometimes it actually works to say just fix it or I’m switching to an alternative, and no, I’m not providing anymore information because I already spelled out the situation twice! (It probably doesn’t work very often, though). Anyway, to celebrate my complacency and the status quo, here’s an updated version of my ad banner script, updated for the new (and simpler) Unity iAd API and with Prime31 iAd/AdMob options as a bonus. And hey, I’ve now got Chartboost set up (via the Prime31 plugin), so if those iAd dollars go missing agin, I’m ready to switch. I really mean it this time!

    public class AdBanner : MonoBehaviour { public bool showOnTop = true; public string AdMobID = ""; #if UNITY\_IPHONE && FUGU\_ADS && P31\_IAD void Start() { AdBinding.createAdBanner (!showOnTop); } #endif #if UNITY\_IPHONE && FUGU\_ADS && !P31\_IAD private ADBannerView banner = null; void Start() { GameObject.DontDestroyOnLoad(gameObject); // keep ad alive if we load a new scene banner = new ADBannerView(ADBannerView.Type.Banner,showOnTop ? ADBannerView.Layout.Top : ADBannerView.Layout.Bottom); ADBannerView.onBannerWasLoaded += OnBannerLoaded; } void OnBannerLoaded() { Debug.Log("Ad banner Loaded!n"); banner.visible = true; } #endif #if UNITY\_ANDROID && FUGU\_ADS void Start() { AdMobAndroid.init(AdMobID); AdMobAndroid.createBanner(AdMobAndroidAd.smartBanner, showOnTop ? AdMobAdPlacement.TopCenter : AdMobAdPlacement.BottomCenter); } #endif }
