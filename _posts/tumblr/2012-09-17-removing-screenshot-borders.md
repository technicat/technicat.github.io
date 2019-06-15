---
layout: post
title: Removing Screenshot Borders
date: '2012-09-17T14:06:49-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612440901/removing-screenshot-borders
---
Upgrading from Snow Leopard to Mountain Lion fixed one of my screenshot problems - full-screen window captures were lopping off a portion of the window, possibly due to the surrounding transparent shadow that is added. What I really want is to remove the shadow, and I found the right Terminal magic on [krypted.com](http://krypted.com/):

`defaults write com.apple.screencapture disable-shadow -bool TRUE
504 sudo killall SystemUIServer`

