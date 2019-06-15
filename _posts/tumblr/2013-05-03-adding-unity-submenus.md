---
layout: post
title: Adding Unity Submenus
date: '2013-05-03T17:56:18-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612477706/adding-unity-submenus
---
This &nbsp;is probably one of those things that everyone else knows and I only just figured out, but I’ve been wondering how to take my Editor-scripted HyperBowl menu items and put them in a submenu of my FuguGames menu (menu bar space is scarce). Turns out it’s just a matter of treating the menu name like a pathname. For example, where before I just specified “HyperBowl/Tokyo” to add a Tokyo item to the HyperBowl menu (to configure the Player Settings for a HyperBowl Tokyo build), now it’s “FuguGames/HyperBowl/Tokyo” to place it in a HyperBowl submenu of the FuguGames menu.  
`
[MenuItem ("FuguGames/HyperBowl/Tokyo")]
static void Tokyo() {
PlayerSettings.productName = "HyperBowl Tokyo";
PlayerSettings.bundleIdentifier = "com.technicat.HyperTokyo";
PlayerSettings.SetScriptingDefineSymbolsForGroup(BuildTargetGroup.iPhone,"HYPERTOKYO;"+freeDefs);
UseIcon ("tokyo.png");
}`

