---
layout: post
title: HyperBowl in Unity Flash
date: '2012-01-06T12:53:11-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515808921/hyperbowl-in-unity-flash
---
HyperBowl is now running in Flash, more or less, on the [HyperBowl web site](http://hyperbowl3d.com/), courtesy of the Unity 3.5 Developer Preview - just click on the Play Flash button to try it out. And you can click on the Play Unity button for the webplayer for a side-by-side comparison (spoiler alert - the Unity webplayer is faster).

It took two days for the conversion. Here’s a quick summary of what I had to do to get it working:

Removed the mouse control and just use AWSD/arrow keys to bowl, since GetAxis wasn’t returning good values for the mouse (at least on Mac)

Turned off shadows for performance (had to do that for each light since it didn’t seem to respect the Quality setting)

Adjusted the fps display code since ToString won’t take “f2” as an argument

Removed call to System.GC.Collect since the compiler doesn’t recognize System.GC

Removed the M2H Localization package due to a duplicate-definition error in the resulting as file (maybe due to a big case statement in the cs script)

Closed off the San Francisco and Tokyo lanes due to a “null” error displayed onscreen at runtime - those lanes are the biggest so maybe I ran into a resource limit.

Removed all script calls that were setting large audiosource mindistances - that was causing loud distortion.

Had to add inner parentheses to an expression of the form “if ( transform.position.y\<miny || transform.position.x\<minx || …” for it to return correct values.

Vertex-lit materials with emissive components weren’t emitting - replaced them with unlit textures.

Replaced iTween.cs with the one tweaked for Unity Flash by David Reimer and used the Unityscript workarounds provided by others in the comments (uninlining hashtables, specifying whole vectors instead of components)

Changed all my deferred-lighting cameras to forward rendering path.

Removed all the image effects (I was getting an error in the Depth of Field effect but for expediency got rid of them all)

Remove calls to ExternalEval

Implement own OnMouseDown/Enter/Exit

