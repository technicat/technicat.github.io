---
layout: post
title: Mac App Store Tips
date: '2011-04-11T00:30:42-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110412025511/mac-app-store-tips
---
Although I’m bailing out of the Mac App Store (I’m even going to ask for a refund of the developer fee, really to emphasize my objection to their rejection of [HyperBowl](http://hyperbowl3d.com/) - Schoolhouse Rock, anyone? - I wouldn’t mind the money back, though), I’ve made enough Mac App Store builds to have some tips: First, read the [Blurst blog](http://technology.blurst.com/unity-games-and-mac-app-store/) that explains in detail how to prepare a Unity MacOSX build for the Mac App Store. The procedure involves some tedious details after the Unity build so it’s a good idea to script some of it. For example, I have the final steps listed in the Blurst blog in a shell script like this:

    chmod -R a+xr FuguMaze.app codesign -f -v -s "3rd Party Mac Developer Application: Technicat, LLC" "FuguMaze.app" productbuild --component "FuguMaze.app" "/Applications" --sign "3rd Party Mac Developer Installer: Technicat, LLC" "FuguMaze.pkg"

Also, it’s a good idea to make a copy of the final info.plist and icons file outside of the app so it doesn’t get clobbered with each build. In fact, the script would be better if it performed a copy of those files into the app and also had a variable in place of the app name so you could use it more easily among multiple apps.
