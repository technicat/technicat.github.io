---
layout: post
title: Unity 3.5 iAds (corrected)
date: '2012-05-20T15:33:00-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515861126/unity-35-iads-corrected
---
I think Unity 3.5 still has some performance issues on mobile, at least Android, but there are some convenient new features for mobile. On Android, I like the spinning load cursor. On iOS, my favorite new feature is the iAd support. I’ve been using the prime31 iAd plugin with no problems, but if the feature is built into Unity, so much the better. I posted my code for bringing up a banner ad a while ago, based on the example in the Unity script reference, but I made a crucial error - I thought I improved the code by moving the banner variable declaration into the ShowBanner function, but that allows it to get garbage collected, and after a while the ad stops refreshing (that is the second garbage-collection error I’ve made in the last few months - as a one-time Lisp programmer, I’m quite embarrassed). So here’s the corrected version:

``

var banner:ADBannerView;

function Start () {  
GameObject.DontDestroyOnLoad(this);  
StartCoroutine(ShowBanner());  
}

function ShowBanner() {  
banner = new ADBannerView();  
banner.autoSize = true;  
banner.autoPosition = ADPosition.Top;  
while (!banner.loaded && banner.error == null)  
yield;

if (banner.error == null)  
banner.Show();  
else banner = null;  
}

I’ve tested that code in a submitted app, [Fugu Match](http://itunes.apple.com/us/app/fugu-match/id450691603), and the revenue is coming in, so it seems to be working fine.

There’s also support for interstitial ads, which I’d forgotten I added to [Fugu Type](http://itunes.apple.com/app/fugu-type/id361179164) (I only realized it when I saw I was getting a little bit of ad revenue). I don’t see a code example in the script reference, but here’s what I’m using, which is pretty simple.

`
function Start() {
if (iPhone.generation == iPhoneGeneration.iPad1Gen || iPhone.generation == iPhoneGeneration.iPad2Gen || iPhone.generation == iPhoneGeneration.iPad3Gen) {
var ad = new ADInterstitialAd();
while (!ad.loaded) yield;
ad.Present();
}
}`

