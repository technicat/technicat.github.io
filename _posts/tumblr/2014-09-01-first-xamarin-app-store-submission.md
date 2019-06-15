---
layout: post
title: First Xamarin App Store Submission
date: '2014-09-01T09:14:45-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110698056141/first-xamarin-app-store-submission
---
Well, after nearly a year (uh oh, that annual subscription fee is coming soon), I submitted an app built with Xamarin to the App Store. Now the suspense begins with the Apple review process, although I’m using cross-platform Xamarin Forms with the idea that I can always build an Android version (never mind that the Android build fails with a mysterious apparent compilation error).

There’s a decent amount of Xamarin documentation, but with Forms especially, seems like I have to figure out some stuff myself. For example, to test on my device, I have to select the target by the Run button but actually use the right-click Run button on the iOS platform item in the project list. And it seems like using the GUI app icon selectors doesn’t work - I have to name my icons with those non-descriptive Icon@2x.png names and so on.

On the other hand, you really should read the documentation when it comes to the App Store upload phase - although Xamarin prompts you to install and use the Application Loader (which might work, except I can’t figure out where you’re supposed to find the archive file when the loader asks for it), just do what the doc says and use the Xcode Organizer to submit the archive, like I do with Unity (ah, Unity!).

[![Screen Shot 2014-08-31 at 8.37.12 PM](http://itshardtofondlepenguins.com/wp-content/uploads/2014/09/Screen-Shot-2014-08-31-at-8.37.12-PM.png)](http://itshardtofondlepenguins.com/wp-content/uploads/2014/09/Screen-Shot-2014-08-31-at-8.37.12-PM.png)

