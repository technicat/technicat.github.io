---
layout: post
title: An NSIS Installer for Unity.
date: '2011-04-13T14:13:15-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412027051/an-nsis-installer-for-unity
---
For Windows builds, Unity generates an exe file and an accompanying data folder that has to reside in the same directory at runtime. I use the open source [NSIS](http://nsis.sourceforge.net/) installer generator with a reusable installer script to generate installers. There is a [Unity setup file](http://svn.technicat.com/technsis/unity.nsi),[generic setup file](http://svn.technicat.com/technsis/setup.nsi),[files list](http://svn.technicat.com/technsis/unityfiles.nsi), and an [uninstaller script](http://svn.technicat.com/technsis/unityunfiles.nsi).

1. Place the four NSIS scripts in directory.
2. Place the Unity-generated EXE file and data folder in an adjacent directory, and optionally a license file, readme file and icon (ICO) file.
3. Edit unity.nsi with the name of the adjacent directory, your company name, the app name, and optional properties like the installer screen and icon (comment them out if you don’t have them)
4. Compile unity.nsi with NSIS. The installer executable will show up in the same directory.
Here’s how I set up the folders for the [HyperBowl Windows build on GameJolt](http://gamejolt.com/freeware/games/arcade/hyperbowl/4977/).[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/Screen-shot-2011-04-13-at-11.06.45-AM.png "Screen shot 2011-04-13 at 11.06.45 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/Screen-shot-2011-04-13-at-11.06.45-AM.png)[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/Screen-shot-2011-04-13-at-11.06.18-AM.png "Screen shot 2011-04-13 at 11.06.18 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/04/Screen-shot-2011-04-13-at-11.06.18-AM.png)
