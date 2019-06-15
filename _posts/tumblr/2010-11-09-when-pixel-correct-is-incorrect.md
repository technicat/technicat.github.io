---
layout: post
title: When Pixel Correct Is Incorrect
date: '2010-11-09T03:08:12-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411982091/when-pixel-correct-is-incorrect
---
The nice thing about 3D is that it’s resolution-independent. So it is with some smugness that I’ve seen my Unity 3D apps scale nicely with the iPad and the 4th-generation iPhone and iPod touch while 2D developers have to scramble to convert their assets (never mind they can just sell them as “HD” apps and charge more). But I do have some 2D elements, e.g. on-screen help text using GUIText. Fortunately, there’s a quick fix. By default, GUIText has its pixel-correct checkbox on, which specifies the text will be displayed at the imported font resolution.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/11/Screen-shot-2010-11-08-at-11.54.52-PM.png "Screen shot 2010-11-08 at 11.54.52 PM")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/11/Screen-shot-2010-11-08-at-11.54.52-PM.png)

Uncheck the box, and you can scale it. Also, more important for my purposes here, the text will scale (implicitly, with the GUI coordinate system) with the screen resolution. The text isn’t as crisp as before, but then again, I don’t have to write code that swaps fonts.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/11/IMG_0235.png "IMG\_0235")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/11/IMG_0235.png)

