---
layout: post
title: Unity Shadow Checklist
date: '2012-04-22T13:22:02-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515849006/unity-shadow-checklist
---
The Unity version of HyperBowl started out as a webplayer and was eventually ported to iOS and later to Android. Now I’ve close the loop by porting the new Snowpark lane from Android back to a webplayer. In doing so, I tried to add effects that I would have been removing in the other direction, like dynamic shadows. This turned out to be a good way to rediscover every possible thing that can disable shadows. So if you don’t see the dynamic shadows you’re expecting, here’s a checklist:

- Make sure you’re using Unity Pro
- Check your current Quality Settings and make sure dynamic shadows are enabled.
- Check your camera’s rendering path - you can use forward rendering if you just have one directional light casting shadows, use deferred rendering if you need more.
- Check your shadow casting light - make sure the culling mask is set so that it’s lighting/shadowing what you think it is, make it directional if you need soft shadows or if you’re using forward rendering, check the shadow intensity and other shadow settings.
- Check the mesh components on all the shadowing and shadowed objects - make sure the receive and cast shadows checkboxes are checked as desired.
- In the Render Settings check the shadow distance setting. Make sure it’s far enough for all your shadows, but also you can optimize a bit by making it near enough to avoid the cost of shadows you don’t want to or can’t see.
