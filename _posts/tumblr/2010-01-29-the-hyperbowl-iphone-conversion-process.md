---
layout: post
title: The HyperBowl iPhone Conversion Process
date: '2010-01-29T02:27:39-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318420616/the-hyperbowl-iphone-conversion-process
---
Each release of [HyperBowl](http://hyperbowl3d.com/) for the iPhone is a bit of an ordeal, since main development takes place on the web player version with Unity Pro, and I have to copy that latest snapshot to Unity iPhone and then hack away at it until it runs at an acceptable frame rate. Sometimes I forget an optimization or two that I’d made in a previous release, so this seems as good a time as any to jot down the steps. These are what I remember now - if I missed any, I hope they’ll come back to me as soon as I start.

1. Duplicate the Unity Pro project, open up the new project in Unity iPhone, watch it convert.
2. In the Player Settings, set the game name
3. In the Player Settings, set the most aggressive speed and code stripping settings
4. Copy the splash screen and icon files into the project, assign them in the Player Settings
5. Replace control and option scripts with iPhone counterparts
6. Set Static on all static game objects
7. Assign batching script to object groups that move together
8. Replace certain materials (like bump maps) with simpler ones
9. Change diffuse materials to vertex lit
10. Remove transparent objects as necessary
11. Remove lights as necessary
12. Remove particle effects as necessary
13. Remove blob shadows as necessary
14. Replace Unity water with simple water
15. Use the iPhone background shader for the background
16. Replace Ogg Vorbis sound with uncompressed or m4a sounds
17. Replace any DXT compressed textures with PVRTC compressed textures
18. Set accelerometer frequency to zero
And of course, profile, profile, profile…
