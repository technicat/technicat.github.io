---
layout: post
title: Unity vs. Xamarin
date: '2014-12-31T06:03:00-08:00'
tags:
- unity
- xamarin
- ios
- android
tumblr_url: https://fugugames.tumblr.com/post/110698090091/unity-vs-xamarin
---
Comparing Unity with Xamarin is sort of apples and oranges - after all, I’m using both, one for game apps and the for, well, non-game apps. But still, there are some interesting similarities and differences.

Both use Mono. In fact, as I understand it, Unity licensed Mono from Xamarin. So, naturally, both feature C#, but Xamarin is also introducing F#, and Unity has their own version of Javascript, and Boo, although I think they’re deprecating the latter two.

Unity also licensed MonoDevelop from Xamarin, but the Xamarin version works better. A lot better. Unity’s version has improved a lot (it used to drive me nuts), but features like Find References work like a charm in Xamarin’s version, and I’m kind of amazed it doesn’t fall apart when I rename or move files in the Xamarin Studio project, while with Unity I’m basically using MonoDevelop as a simple text editor.

Unity does a have a nice built-in bug reporter, which also helpfully pops up when the Unity Editor crashes. With Xamarin, you have to submit a report to their bugzilla. On the other hand, you can actually browse their bugzilla, and I’ve always got a quick response from someone who seemed like they might be an engineer. With Unity, in the old days, I used to get bug responses from Unity devs, but now they’re popular, they have gatekeepers who sometimes seems to be a newbie who assumes you’re a newbie.

Unity does a have a wider range of support platforms: the answer site, the feedback site, the bug vote site, and the beta lists. Both Unity and Xamarin have forums. I’d have to say the Xamarin forums have better questions and answers, although the Unity forums again have more variety. But like the bug reporting, the forums are victims of Unity’s popularity, so after the umpteenth can-you-fix-my-code-just-tell-me-what-to-do question, I stay away. The beta lists are like the cool clubs - the only thing is, you have to use stuff that’s in beta.

The Unity Asset Store is awesome. Xamarin has a Component Store and a NuGet repository, which are pretty useful, but it’s like comparing a 7-11 to a Walmart (or if you hate, Walmart, say Costco or Target).

Cross-platform in Unity is a breeze. Build-and-run, switch platforms, build-and-run. Xamarin enables some code-sharing among platforms since it’s Mono, but for the most part app development involves direct C# mappings to native APIs. They did introduce a least-common-denominator cross-platform API in Xamarin Forms this year, but I found it to be still flakey (I managed to deploy one app on iOS and Android, but was unable to update because it started complaining about missing references)

Conversely, Xamarin gives you comprehensive access to the native APIs (Xamarin Forms aside), while in Unity you’re gonna need a plugin, and if you find the plugins you need, you have to watch out for conflicts among them.

Finally, Xamarin has an annual licensing model, while Unity offers both licensing and purchase, although I have to pay for an upgrade every couple of years, so you could argue it’s not that much different from licensing (especially since renewing your Xamarin license just means you get upgrades - if you fail to renew, I’ve been told, you can still use your current installation).

I’m paying $300 every year each for an iOS and Android Xamarin Indie license, compared to typically $750 each for Unity desktop, iOS and Android upgrades every couple of years. So Xamarin is cheaper, although I’m comparing Indie to Pro (Xamarin has a couple of tiers above Indie). Xamarin has a free Starter edition while Unity has a free Basic or Indie license. Unity Indie is pretty useful (they keep moving Pro features into Indie to placate the mob), while Xamarin Starter is pretty useless if you try to make any kind of interesting app (limited in size and API).

Cutting to the chase, looking at revenue, I’m making a few thousand a year from Unity, and so far zip from Xamarin except for consulting and work-fore-hire stuff, but I just started with Xamarin a year ago, so check with me later. Educationally, Unity is great for learning 3D graphics and game dev, while Xamarin is great for learning near-native development without having to stare at Objective-C code or use Eclipse. If you can use both, maybe even share some C# familiarity and code between the two, that’s not a bad way to go.

