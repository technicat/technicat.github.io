---
layout: post
title: A Really Small Unity Web Player
date: '2010-02-27T15:02:46-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318426466/a-really-small-unity-web-player
---
How small can you make a Unity web player? Well, I haven’t bothered to try building an empty scene to see its size, but it must be less than 20K, because my menu scene on [Fugu Games](http://fugugames.com/)is 19,534 bytes. I wouldn’t say it’s imperative to make it that small, but it is the first scene that automatically loads on the site’s home page, so it should load reasonably quickly for anyone, anywhere (as long as they’re on a platform that supports the Unity web plugin). And if some Flash developer starts acting superior about file sizes, you can retort “can you do 3D in&nbsp; 20k?”.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-19.png "Picture 19")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-19.png)

There isn’t much to this scene - just some textured spheres scripted to constantly look at the mouse position (just in case you didn’t realize this is 3D), a single directional light (again, 3D), and some mouseover and mouseclick behavior, the latter which loads the bigger players (some of which could use a Biggest Loser treatment).

Even with this simple example, it took a little effort to squeeze it down. One standard technique - scale down the textures size. The original size of the texture is overkill for small spheres. Setting the max texture size to 256 didn’t noticeably degrade the graphics (although 128x128 started to look coarse).

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-16.png "Picture 16")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-16.png)

A less obvious source of unnecessary texture size is the font. There’s just one font here, but we’re certainly not using the whole Unicode character set. And I decided I didn’t really need mixed-case text.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-18.png "Picture 18")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/02/Picture-18.png)

Finally, I removed the Pro and Standard Assets from the project, primarily to remove the scripts I’m not using. Even unused scripts are built into the web player.

