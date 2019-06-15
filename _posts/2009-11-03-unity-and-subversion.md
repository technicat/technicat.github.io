---
layout: post
title: Unity and Subversion
date: '2009-11-03T18:33:38-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318401366/unity-and-subversion
---
I was pleasantly surprised to find that my number one feature request showed up in the latest [Unity](http://unity3d.com/) release - [svn](http://subversion.tigris.org/) support. But after following the instructions in the Unity manual on how to import an existing project into svn and check it out again (last link in the Advanced Topics section of the TOC), I realize “svn support” doesn’t mean svn integration in the Unity Editor - it’s really more accurately stated as svn compatibility, accomplished by writing an additional .meta file for each asset (which seems to slow file manipulation in the Project window a bit, but you can turn off the svn compatibility at least temporarily if that bothers you).

Every time you add/move/rename/delete/change a file in the Editor, you have to sync that with your svn repository outside of Unity (in my case, typing svn commands in the Mac Terminal window). It’s a bit inconvenient, but doable - after a batch of changes, I’ll go to the shell, type “svn commit”, and if it complains that something is missing because I moved/renamed/deleted a file or folder, I just “svn delete” it and try again.

Also, you’re probably going to grumble a bit after checking out a newly-imported project if you’ve already been working on it for a while. In following the Unity instructions, the assets come through fine but you lose the global settings. For example, I found my custom Quality and Player settings wiped out, and most exasperatingly, all the Layer names. Objects still retain their layer bitmask settings, but any object set to a custom layers shows that layer name unhelpfully as blank (during a long bath, I figured out I could deduce the original layer names by typing in dummy names such as “layer1”, “layer2”, etc. and then rename them to their proper names after seeing which objects they were assigned to. Considering all the bugs I’ve fixed/worked-around during tub soaks, I should have deducted that bathroom remodel as a business expense!)

Despite the non-seamless use, I’m pretty sure I’ll be sticking with Unity+svn. Time Machine is great, and I’ll still make periodic DVD burns, but there’s no substitute for version-controlled backups located offsite. And now I can “svn diff” my scripts instead of blindly saving them. I hope I can do the same with the next version of Unity iPhone.

