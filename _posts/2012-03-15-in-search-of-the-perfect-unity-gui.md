---
layout: post
title: In Search of the Perfect Unity GUI
date: '2012-03-15T15:14:20-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515836116/in-search-of-the-perfect-unity-gui
---
The biggest impediment to game development in Unity is GUI creation, to the point where every new feature or new app that I consider implementing starts with me groaning, “but I’ll have to add a user interface for that”. Unity’s not alone in this issue - there is a reason Scaleform is so popular. Nevertheless, this is why I’m on my third purchase of a third-party GUI package in the past year (almost $500 spent on all three!).

The first was GUIKit001, which has the disadvantages of a UnityGUI-based system (not great performance on mobile, not particularly suited for multiple screen resolutions) but also the advantages (nice to have your whole GUI in one script), and looked a lot better than my own UnityGUI-based pause menu (it’s free on the Unify community wiki).

I stuck with that for a while until I ran into graphical corruption issues with UnityGUI on Android, especially on the Nook Color, so I decided a 3D GUI-based system was the way to go and invested in EZGUI, which appeared to be the most popular. That worked, HyperBowl and Fugu Bowl still use GUIKit001 but the rest are now on EZGUI. However, it’s a big system and there’s that “hello world” issue - it’s not easy to get something simple up and running quickly.

Which leads me to candidate number three, NGUI. I saw a lot of good reviews for it, the documentation is available publicly on the product web site, the support forums (on the Unity forum and the product web site) are very active, it’s under a hundred bucks and some money from my Fugu Maze project (which by the way features my old pause menu) on the Asset Store came in, so I had some paypal money burning a hole in my pocket and decided let’s give it a whirl (too bad I bought just before it went on a 20% sale).

It is easy to get something simple up and running quickly. I decided my little [Fugu System](https://play.google.com/store/apps/details?id=com.technicat.fugusystem) info display app could benefit from an email button, so first I created a UI layer in Unity, then invoked the NGUI Create UI wizard, selected that layer:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-14-at-12.34.24-PM.png "Screen shot 2012-03-14 at 12.34.24 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-14-at-12.34.24-PM.png)

That instantiates a UI camera, anchor and panel in the project. Another wizard creates individual widgets, in this case a button, and I used the texture atlas from one of the samples:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-14-at-12.36.04-PM.png "Screen shot 2012-03-14 at 12.36.04 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-14-at-12.36.04-PM.png)

Finally, I set the anchor to bottom-right and entered an offset in the button transform so it stays completely on-screen (here I felt like I was typing in mystery numbers - I do prefer working in normalized screen coordinates) And here’s the result. It does seem to have a very clean and simple component model. To add the click-to-email behavior, I just attached a script to the button with an OnClick callback that calls the email function in the Etcetera plugin from Prime31 Studios.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-15-at-12.25.45-AM.png "Screen shot 2012-03-15 at 12.25.45 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/03/Screen-shot-2012-03-15-at-12.25.45-AM.png)

