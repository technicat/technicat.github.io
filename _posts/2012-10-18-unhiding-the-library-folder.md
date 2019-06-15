---
layout: post
title: Unhiding the Library Folder
date: '2012-10-18T22:45:28-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612447641/unhiding-the-library-folder
---
If I had Apple stock to sell, I would sell it, not because of important issues like worker exploitation in China or abuse of the patent system, but because they’re doing stupid things like hiding the Library folder. It’s a real pain in the ass, for example, when I’m trying to access screenshots taken in Xcode. Typing the following in Terminal will undo the damage:

`chflags nohidden ~/Library`

