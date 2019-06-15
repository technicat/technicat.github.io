---
layout: post
title: Inspecting the Android Manifest (again)
date: '2012-01-17T18:01:49-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515814746/inspecting-the-android-manifest-again
---
A while ago I blogged a tip on how to see what’s in your Unity-generated Android manifest file, by inspecting file in your project’s temp/stage directory right after you perform a build. However, that directory disappears when you change projects or exit Unity. What to do after that? Use the aapt tool in your Android SDK (under the platform-tools directory), like this:

`
aapt dump xmltree HyperBowl.apk AndroidManifest.xml`

which will print out the contents:

`
N: android=http://schemas.android.com/apk/res/android
  E: manifest (line=2)
    A: android:versionCode(0x0101021b)=(type 0x10)0x20
    A: android:versionName(0x0101021c)="3.15" (Raw: "3.15")
    A: android:installLocation(0x010102b7)=(type 0x10)0x2
    A: package="com.technicat.HyperBowl" (Raw: "com.technicat.HyperBowl")
    E: supports-screens (line=3)
      A: android:anyDensity(0x0101026c)=(type 0x12)0xffffffff
      A: android:smallScreens(0x01010284)=(type 0x12)0xffffffff
      A: android:normalScreens(0x01010285)=(type 0x12)0xffffffff
      A: android:largeScreens(0x01010286)=(type 0x12)0xffffffff
      A: android:xlargeScreens(0x010102bf)=(type 0x12)0xffffffff
    E: application (line=4)
      A: android:label(0x01010001)=@0x7f050029
      A: android:icon(0x01010002)=@0x7f020000
      A: android:debuggable(0x0101000f)=(type 0x12)0x0
      E: activity (line=5)
        A: android:label(0x01010001)=@0x7f050029
        A: android:name(0x01010003)="com.unity3d.player.UnityPlayerActivity" (Raw: "com.unity3d.player.UnityPlayerActivity")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xb0
        E: intent-filter (line=6)
          E: action (line=7)
            A: android:name(0x01010003)="android.intent.action.MAIN" (Raw: "android.intent.action.MAIN")
          E: category (line=8)
            A: android:name(0x01010003)="android.intent.category.LAUNCHER" (Raw: "android.intent.category.LAUNCHER")
      E: activity (line=11)
        A: android:label(0x01010001)=@0x7f050029
        A: android:name(0x01010003)="com.unity3d.player.VideoPlayer" (Raw: "com.unity3d.player.VideoPlayer")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xb0
      E: activity (line=14)
        A: android:name(0x01010003)="com.google.ads.AdActivity" (Raw: "com.google.ads.AdActivity")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xb0
      E: activity (line=15)
        A: android:name(0x01010003)="com.prime31.EtceteraProxyActivity" (Raw: "com.prime31.EtceteraProxyActivity")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: configChanges="keyboardHidden|orientation" (Raw: "keyboardHidden|orientation")
      E: activity (line=17)
        A: android:name(0x01010003)="com.prime31.WebViewActivity" (Raw: "com.prime31.WebViewActivity")
        A: android:configChanges(0x0101001f)=(type 0x11)0x80
      E: activity (line=19)
        A: android:name(0x01010003)="com.prime31.P31VideoPlayerActivity" (Raw: "com.prime31.P31VideoPlayerActivity")
        A: android:configChanges(0x0101001f)=(type 0x11)0xb0
      E: activity (line=21)
        A: android:theme(0x01010000)=@0x1030006
        A: android:label(0x01010001)="IntroFlow" (Raw: "IntroFlow")
        A: android:name(0x01010003)="com.openfeint.internal.ui.IntroFlow" (Raw: "com.openfeint.internal.ui.IntroFlow")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xa0
      E: activity (line=22)
        A: android:theme(0x01010000)=@0x1030006
        A: android:label(0x01010001)="Dashboard" (Raw: "Dashboard")
        A: android:name(0x01010003)="com.openfeint.api.ui.Dashboard" (Raw: "com.openfeint.api.ui.Dashboard")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xa0
      E: activity (line=23)
        A: android:theme(0x01010000)=@0x1030006
        A: android:label(0x01010001)="Settings" (Raw: "Settings")
        A: android:name(0x01010003)="com.openfeint.internal.ui.Settings" (Raw: "com.openfeint.internal.ui.Settings")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xa0
      E: activity (line=24)
        A: android:theme(0x01010000)=@0x1030006
        A: android:label(0x01010001)="NativeBrowser" (Raw: "NativeBrowser")
        A: android:name(0x01010003)="com.openfeint.internal.ui.NativeBrowser" (Raw: "com.openfeint.internal.ui.NativeBrowser")
        A: android:screenOrientation(0x0101001e)=(type 0x10)0x1
        A: android:configChanges(0x0101001f)=(type 0x11)0xa0
    E: uses-permission (line=28)
      A: android:name(0x01010003)="android.permission.INTERNET" (Raw: "android.permission.INTERNET")
    E: uses-permission (line=29)
      A: android:name(0x01010003)="android.permission.ACCESS_NETWORK_STATE" (Raw: "android.permission.ACCESS_NETWORK_STATE")
    E: uses-permission (line=30)
      A: android:name(0x01010003)="android.permission.BLUETOOTH" (Raw: "android.permission.BLUETOOTH")
    E: uses-permission (line=31)
      A: android:name(0x01010003)="android.permission.BLUETOOTH_ADMIN" (Raw: "android.permission.BLUETOOTH_ADMIN")
    E: receiver (line=32)
      A: android:name(0x01010003)="com.google.ads.InstallReceiver" (Raw: "com.google.ads.InstallReceiver")
      A: android:exported(0x01010010)=(type 0x12)0xffffffff
      E: intent-filter (line=33)
        E: action (line=34)
          A: android:name(0x01010003)="com.android.vending.INSTALL_REFERRER" (Raw: "com.android.vending.INSTALL_REFERRER")
    E: uses-feature (line=37)
      A: android:glEsVersion(0x01010281)=(type 0x11)0x20000
    E: uses-feature (line=38)
      A: android:name(0x01010003)="android.hardware.touchscreen.multitouch" (Raw: "android.hardware.touchscreen.multitouch")
      A: android:required(0x0101028e)=(type 0x12)0xffffffff
    E: uses-sdk (line=39)
      A: android:minSdkVersion(0x0101020c)=(type 0x10)0x6
      A: android:targetSdkVersion(0x01010270)=(type 0x10)0xe`

