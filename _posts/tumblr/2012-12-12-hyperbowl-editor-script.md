---
layout: post
title: HyperBowl Editor Script
date: '2012-12-12T16:59:22-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612459341/hyperbowl-editor-script
---
It’s the little things. I think my favorite Unity 4 feature is the ability to add custom preprocessor definitions. It’s not only helpful with runtime code, but also with editor scripts. Here’s the script I use for HyperBowl, allowing me to build any of the free versions or the paid version all from the same project. Maybe it should be a script that runs before every build, but the nice thing about making it a menu item is that I can see the resulting changes in the Player Settings when I invoke it.

`
#pragma strict`

@MenuItem (“HyperBowl/PlayerSettings”)  
static function UpdatePlayerSettings() {  
#if UNITY\_IPHONE  
#if HYPERALL  
 PlayerSettings.productName = “HyperBowl”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowl”;  
#endif  
#if HYPERCLASSIC  
 PlayerSettings.productName = “HyperBowl Classic”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowlClassic”;  
#endif  
#if HYPERROME  
 PlayerSettings.productName = “HyperBowl Rome”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowlRome”;  
#endif  
#if HYPERFOREST  
 PlayerSettings.productName = “HyperBowl Forest”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowlForest”;  
#endif  
#if HYPERSHIP  
 PlayerSettings.productName = “HyperBowl High Seas”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowlHighSeas”;  
#endif  
#if HYPERSF  
 PlayerSettings.productName = “HyperBowl San Francisco”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperSF”;  
#endif  
#if HYPERTOKYO  
 PlayerSettings.productName = “HyperBowl Tokyo”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperTokyo”;  
#endif  
#if HYPERSNOW  
 PlayerSettings.productName = “HyperBowl Snowpark”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowlSnow”;  
#endif  
#endif  
#if UNITY\_ANDROID  
#if FUGU\_ADS  
 PlayerSettings.productName = “HyperBowl Lite”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowl”;  
#else  
 PlayerSettings.productName = “HyperBowl Pro”;  
 PlayerSettings.bundleIdentifier = “com.technicat.HyperBowlPro”;  
#endif  
#endif  
}

