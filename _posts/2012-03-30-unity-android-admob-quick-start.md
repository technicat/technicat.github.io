---
layout: post
title: Unity Android AdMob Quick Start
date: '2012-03-30T11:40:36-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515841636/unity-android-admob-quick-start
---
This is how I have AdMob integrated in [my Unity Android apps](https://market.android.com/developer?pub=Technicat,+LLC).

First, I use the AdMob plugin from [Prime31 Studios](http://prime31.com/).

After importing the plugin into a project, I find the AdMobAndroidBanner and AdMobAndroidManager prefabs and drag them into one of my initial scenes.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-30-at-8.30.56-AM.png "Screen shot 2012-03-30 at 8.30.56 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-30-at-8.30.56-AM.png)

I select the AdMobAndroidBanner object and fill in the ID that’s set up for this app on my AdMob account page.

Up ‘til now, that’s standard operating procedure. Now I modify the script attached to the AdmobAndroidBanner object, because the default ad that shows up on tablets is not what I want, it obscures too much of the screen. So I just comment out that section of the CreateBanner function and use the same-size banner on all devices.

`
// if( isTablet() )
// AdMobAndroid.createBanner( AdMobAndroidAd.tablet300x250, ( Screen.width / 2 ) - 150 * density, 0 );
// else
AdMobAndroid.createBanner( AdMobAndroidAd.phone320x50, ( Screen.width / 2 ) - 160 * density, 0);`

The default script centers the ad banner at the top of the screen. For apps where I want it on the bottom, I modify that last parameter accordingly.

`
// if( isTablet() )
// AdMobAndroid.createBanner( AdMobAndroidAd.tablet300x250, ( Screen.width / 2 ) - 150 * density, 0 );
// else
AdMobAndroid.createBanner( AdMobAndroidAd.phone320x50, ( Screen.width / 2 ) - 160 * density, Screen.height-50*density );`

Finally, (or really, at any time) I run the Generate Android Manifest command in the Prime31 pulldown menu from the menubar.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-30-at-7.12.13-AM.png "Screen shot 2012-03-30 at 7.12.13 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-30-at-7.12.13-AM.png)

Check the Plugins/Android/AndroidManifest.xml file to see that there is indeed information about AdMob now.

Final tip, when upgrading the plugin, it seems the prefabs get clobbered, so I just remove the plugin and prefabs before upgrading and redo the whole thing. It’s just these few steps, so it’s not bad.

