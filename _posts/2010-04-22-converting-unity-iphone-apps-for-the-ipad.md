---
layout: post
title: Converting Unity iPhone Apps for the iPad
date: '2010-04-22T04:10:39-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411919291/converting-unity-iphone-apps-for-the-ipad
---
I just finished getting all my [HyperBowl](http://hyperbowl3d.com/) apps on the App Store as “universal” apps, running on the iPhone and on the iPad. With the latest version of Unity iPhone, it’s pretty easy to get it running on the iPad - just select the appropriate settings in the Player Settings, i.e. iPhone+iPad as the target, and specify an appropriately sized iPad icon and portrait and landscape splash images. HyperBowl runs in portrait mode (in fact, the iPad screen aspect ratio is closer to the original game than the iPhone, so that works out splendidly), so here’s one quick tip - if you’re running only in portrait mode, then you don’t actually need to supply a landscape splash screen. Just make sure you delete the reference to the landscape image file in XCode (it’ll be in red if you didn’t specify it in Unity). That saves a bit of file space in your final app. A more important tip is that Apple will probably complain if you don’t support both sides of each orientation, e.g. if you support only portrait, you still need to support portrait and portrait upside-down. That’s easy to code in Unity, e.g.

    switch (iPhoneInput.orientation) { case iPhoneOrientation.Portrait: if (iPhoneSettings.screenOrientation != iPhoneScreenOrientation.Portrait) { iPhoneSettings.screenOrientation = iPhoneScreenOrientation.Portrait; } break; case iPhoneOrientation.PortraitUpsideDown: if (iPhoneSettings.screenOrientation != iPhoneScreenOrientation.PortraitUpsideDown) { iPhoneSettings.screenOrientation = iPhoneScreenOrientation.PortraitUpsideDown; } break;

With that running in an OnUpdate function, your game will flip as necessary when the user rotates the iPad. (Since I’m deploying as Universal apps, I check if I’m running on an iPad, first - I’ll leave that as an exercise for the reader) That still leaves the splash screen. It took some googling for me to find this, but to get the splash screen to start out in the correct orientation, you need to add the UISupportedInterfaceOrientations key to Info.plist in XCode. It’s similar to UIInterfaceOrientations, but as you might guess, you can add multiple orientations - first add the key, right-click on it to specify the Value Type as Array, and then add what you need.[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/04/Screen-shot-2010-04-21-at-11.57.58-PM.png "Screen shot 2010-04-21 at 11.57.58 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/04/Screen-shot-2010-04-21-at-11.57.58-PM.png)

    

