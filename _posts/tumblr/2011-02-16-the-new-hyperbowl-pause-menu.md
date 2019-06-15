---
layout: post
title: The New HyperBowl Pause Menu
date: '2011-02-16T02:57:38-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412007716/the-new-hyperbowl-pause-menu
---
In game development, user interfaces and HUD’s get no respect. They’re often left until the end of the game project, whereupon it’s realized a lot of work is going to be needed (and then contractors like me are called in). I confess, I’ve been guilty of the same thing with the [HyperBowl](http://hyperbowl3d.com/) pause menu. In the web player, I made do with the pause menu script I posted on the [Unity community wiki](http://unifycommunity.com/wiki), but that script is more an instructional example of the UnityGUI than a polished menu (although maybe with the right GUI skin…) For HyperBowl on the iPhone and iPad, I left it out because I thought my pause menu didn’t look polished enough (I treat the web players more as public prototypes), there were some early reports of performance issues with UnityGUI on iOS, and UnityGUI doesn’t automatically scale with resolutions, so the new Retina displays posed a problem.

But once I started working on the Mac App Store version of HyperBowl (recently submitted), I felt I had to put in something, partly because I was getting some requests for one on the [HyperBowl Facebook page](http://facebook.com/hyperbowl). Rule of thumb - if you’ve procrastinated on a feature for over a year, maybe it’s time to outsource. So I looked at [EZGUI](http://anbsoft.com/) and [GUIKit001](http://gameassets.net/). Since EZGUI is based on SpriteManager and GUIKit uses UnityGUI, in principle I might favor EZGUI’s approach. I’ve never felt really comfortable with UnityGUI - not that it’s hard, it just doesn’t feel right to me. On the other hand, that’s how I feel about using Flash for game UI’s, and I’ve spent the last three years on a contract using [Scaleform](http://scaleform.com/).

GUIKit001 also has the advantage of a webplayer and YouTube demo showing a working and polished pause menu, and that looked like something I could drop in, quickly and expediently. There’s nothing like a good demo.

It took me a weekend to hack GUIKit001 into HyperBowl. I ended up just using the Settings menu and not the full menu set, although I’d love to use the swipe controls for something (selecting bowling balls?) I kept the audio volume slider, removed the music volume slider, added help text and checkbox if you’re using the Magic Mouse (Unity reads wackily higher movement values from the Magic Mouse than other mice, so that really messes up the HyperBowl controls without a scaling factor) I think I’ll remove that Settings title, too.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/02/Screen-shot-2011-02-15-at-11.33.42-PM.png "Screen shot 2011-02-15 at 11.33.42 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/02/Screen-shot-2011-02-15-at-11.33.42-PM.png)

