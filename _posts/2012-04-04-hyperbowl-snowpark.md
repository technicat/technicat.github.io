---
layout: post
title: HyperBowl Snowpark
date: '2012-04-04T20:20:09-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515844131/hyperbowl-snowpark
---
I’m often asked about the possibility of introducing new [HyperBowl](http://hyperbowl3d.com/) lanes beyond the original six, and now I’ve finally done it, with the [HyperBowl Snowpark](http://itunes.apple.com/app/hyperbowl-snowpark/id514069534) lane. It happened because I saw a promotion on the Unity forum for the Fruit Cutter project that’s sold on the Unity Asset Store - the deal was by the asset and get another one free, and I figured, $20, why not (which reminds me, I need to get in on that Unity Asset Store Madness Sale which is ending April 8). Anyway, while browsing my choices of free assets, I saw the Cartoon Snowboard Funpack, which looked like it might make a good HyperBowl lane (it is reminiscent of an unreleased motocross lane developed by the original HyperBowl team).

The Snowpark lane is sort of an exercise in rapid development - I spent four days on it before submitting it to the App Store. I received it as an FBX file, and I don’t know if this happens to everyone but I went through this with all the original HyperBowl assets, I had to manually attach all the textures after importing into Unity.

The next step was figuring out the scale. The default Unity import scale, 0.1, again as usual for me, was not appropriate, way too small. However, while the proper scale as far as realistic dimensions could have been 1, that still seemed too small. Then I tried 10 which I thought looked pretty good, but upon playtesting, the 24-second timer kept running out, so I settled on an import scale of 5. With each iteration I had to adjust the bowling pin, ball and camera placements, so it was somewhat time-consuming.

The next issue was sound. I attached ball collision sounds to all of the gameobjects with meshes, created and assigned physics materials to the objects that could possibly be rolled upon and specified roll sounds for them.

The rest was tweaking and polish - adjusting the camera follow properties (height, damping), setting up the camera flythru, finalizing the shaders, adding a skybox and lens flare and a directional light (which only affects the ball in this lane, as the snowpark textures are prelit).

Fortunately, I didn’t have to do much optimization beyond marking the environment as static. The whole thing is small enough to run at 60fps on my 4th-gen ipod touch (a bit below on my 1st-gen iPad, I suspect due to the lens flare).

Four days ain’t bad, but keep in mind, it’s only four days if you set aside the last three years I’ve spent on HyperBowl, the time I spent last year reorganizing the Unity project so that I could deliver individual lanes, all the work performed ten years ago by the original HyperBowl team, and all the work that went into the various middleware and other assets (including the Funpark) that I used! And oh, yeah, this is actually my second attempt at a new HyperBowl lane. I spent several days on another one, but so far I don’t think it’s fun enough. Which just goes to show, as the risk of turning this into a dry subject, rapid development requires efficient and economical use of work that’s already been done.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2012/04/IMG_0248.png "IMG\_0248")](http://itshardtofondlepenguins.com/wp-content/uploads/2012/04/IMG_0248.png)
