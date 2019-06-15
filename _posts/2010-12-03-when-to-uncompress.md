---
layout: post
title: When to Uncompress
date: '2010-12-03T22:48:05-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411988771/when-to-uncompress
---
Usually when porting a game to a mobile platform, you want to compress, compress, compress. With [HyperBowl on the iOS](http://itunes.apple.com/us/app/hyperbowl/id344209253?mt=8), however, I discovered many of the transparent textures that look decent with DXT5 compression, look mediocre to awful in 4-bit PVRTC. Fortunately, the new multi-platform support in Unity 3 allows me to specify per-platform texture compression settings - in these cases, I switch the texture to 16-bit RGBA.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/12/Screen-shot-2010-12-03-at-11.50.45-AM.png "Screen shot 2010-12-03 at 11.50.45 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/12/Screen-shot-2010-12-03-at-11.50.45-AM.png)

