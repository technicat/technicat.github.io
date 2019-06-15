---
layout: post
title: "(Re)submitting to the Unity Asset Store"
date: '2012-05-03T23:02:26-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515855316/resubmitting-to-the-unity-asset-store
---
Move over Hunger Games, I now have the Fugu Games trilogy on the Unity Asset Store, Fugu Maze, Fugu Type and Fugu Bowl. I put Fugu Maze there a year ago to try out the Asset Store, and the process was painful enough I decided that’s enough for now. But after receiving recent review complaining about an apparent incompatibility with Unity Indie (maybe starting with Unity 3.5, or maybe it’s been there all along and I only had Pro customers), and some import pathname warnings that may or may not have been causing problems, I felt obligated to update the package, and I found the process has really improved. Dare I say, it’s quite slick.

If you haven’t gone through the Asset Store submission process recently, the first thing to do is check out the explanatory [Unity blog](http://blogs.unity3d.com/2012/02/19/how-to-submit-content-to-the-unity-asset-store/). There’s a video introduction, but the really useful thing is the link to download layer masks that you can use for your key images, provided in Photoshop and GIMP formats.

Then import into your project the latest Asset Store Tools from the Asset Store (nice!).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-03-at-5.29.44-PM.png "Screen shot 2012-05-03 at 5.29.44 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-03-at-5.29.44-PM.png)

If you have a really old AssetStoreTools directory like I did, there are probably some obsolete files in there so you might want to just remove the whole thing first. Same with the AssetStore directory that used to hold the key images and other package info. That’s all handled in a new Package Manager window now.

You can bring up that window from the Asset Store Tools menu that should have appeared after your import.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-03-at-5.03.09-PM.png "Screen shot 2012-05-03 at 5.03.09 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-03-at-5.03.09-PM.png)

If this is a new package, select Create Package from the upper left, otherwise select the existing package your’re modifying. One quirk I’ve noticed - sometimes it will switch the selection back to a previous package, so watch out.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-03-at-5.30.19-PM.png "Screen shot 2012-05-03 at 5.30.19 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/05/Screen-shot-2012-05-03-at-5.30.19-PM.png)

Fill this out, hit Preview liberally to see how it looks, use the downloaded key image masks to create your key images. If you’re updating the asset or creating the first version of one, you need to upload the asset (I’ve just done complete projects so I choose the Asset directory of the project) before you submit. If you’re just changing the description, you can just hit Submit, but it will still go through a review. The instructions list only a few supported HTML tags, but it certainly supports more (e.g. the \<a\> tags), but I don’t know how much more.

The other command I regularly use from the menu is the Publisher Admin command, which brings up your Asset Store admin page in a browser. Sometimes the resulting page doesn’t show any data or selectable months - in that case, you need to log into the store separately in the browser, first (which admittedly, defeats the convenience).

One more tip, which may seem obvious. For a while, I couldn’t figure out how to test compatibility with Unity Indie, but then, duh, I realized I could just download Unity Indie on another machine (my Windows laptop which just exists for contract work and Windows testing of my own stuff), registering it with a different email (not quite sure that’s necessary, but it ensures it’s distinct from my Pro license).

