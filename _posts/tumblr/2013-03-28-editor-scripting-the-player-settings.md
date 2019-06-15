---
layout: post
title: Editor Scripting the Player Settings
date: '2013-03-28T13:44:38-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612472801/editor-scripting-the-player-settings
---
A while back, I cleaned up my Unity Editor script that fills in Player Settings for my HyperBowl project, which I use to generate eight distinct iOS apps. Now that script creates a menu and adds a menu item for each of those builds. Below is the menu item for the paid app with all the lanes. It sets the product name, the build ID, preprocessor definitions, and the icons, which were a bit tricky - seems I had to provide exactly four icons, corresponding to the icon overrides in the Player Settings, but there’s no way I can see to set the default icon.

`@MenuItem ("HyperBowl/HyperBowl")
static function HyperBowl() {
	PlayerSettings.productName = "HyperBowl";
	PlayerSettings.bundleIdentifier = "com.technicat.HyperBowl";
	PlayerSettings.SetScriptingDefineSymbolsForGroup(BuildTargetGroup.iPhone,"HYPERALL");
	var icons:Texture2D[] = new Texture2D[4];
	icons[0]=AssetDatabase.LoadMainAssetAtPath("Assets/iPhoneTextures/Icon/hyperbowl-logo-banner-scaled-512x512.png");
	icons[1]=AssetDatabase.LoadAssetAtPath("Assets/iPhoneTextures/Icon/hyperbowl-logo-banner-scaled-114x114.png",Texture2D);
	icons[2]=AssetDatabase.LoadAssetAtPath("Assets/iPhoneTextures/Icon/hyperbowl-logo-banner-scaled-72x72.png",Texture2D);
	icons[3]=AssetDatabase.LoadAssetAtPath("Assets/iPhoneTextures/Icon/hyperbowl-logo-banner-scaled-57x57.png",Texture2D);
	PlayerSettings.SetIconsForTargetGroup(BuildTargetGroup.iPhone,icons);
}`

