---
layout: post
title: Xamarin Gotchas
date: '2014-07-16T10:23:58-07:00'
tags:
- xamarin
tumblr_url: https://fugugames.tumblr.com/post/110698044826/xamarin-gotchas
---
Xamarin is one of those tools that I’ve been interested in using, but it’s taken a while to get some traction. I purchased Android and iOS licenses last fall, but I had some initial trouble with the Android samples on github - just to get them running, I had to tweak the project settings (increase the maximum java heap size and uncheck use-latest-sdk due to problems with sdk-19). And really, C# isn’t really a higher level language than Java (some might say a copy), so it’s not so obvious it’s a win on Android.

On the other hand, I have no desire to program in Objective-C, so Xamarin iOS is appealing. I returned to Xamarin for iOS development just recently (after a brief flirtation with their new Forms cross-platform framework, but maybe it’s a bit too new - I ran into problems right after just copying a project from one directory to another).

So far, it’s been pretty good - the build-and-run works smoothly, a bit more smoothly even than Unity (Xamarin doesn’t make you manually use Xcode), and much more smoothly than Android (adb always got confused and required refresh/restart to show the test device, a problem I don’t have with Unity Android). And Xamarin’s publish-to-TestFlight feature is fantastic, notwithstanding the uncertain future of TestFlight.

However, using a middleware layer means a new layer of problems, which take a lot of time to figure out via searching (and even more time when I forget to make a note of it and have to go through all that again later).

For example, one gotcha, I had to enable their new reference counting system to avoid null references when referencing text fields in UIAlertView dialogs. Another, it seems that UIGestureRecognizer requires the target action to be specified in the constructor like this:  
`
UIGestureRecognizer gesture = new UITapGestureRecognizer (
				(g)=> { 
					// action
				});`

or it will fail to compile or crash. Still, better than Objective-C, so I’ll probably stick with it until Swift is stable.

