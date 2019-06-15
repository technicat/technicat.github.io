---
layout: post
title: Itty Bitty Bug Report
date: '2012-09-01T19:43:43-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612436131/itty-bitty-bug-report
---
More normal approach to non-critical Unity bugs is wait a few months for someone else to report them, and then go ahead and report them while I’m procrastinating on other things. Case in point, I just submitted a bug report that the following code in an initially active object does not mute a sound that that is active and has PlayOnAwake selected.

`function Start() {
AudioListener.pause = true;
}`

I noticed this a while back with the pause menu that I have on the wiki/assetstore/github - sound is muted when the menu is brought up mid-game but not if its up at the beginning (in particular, the soundtrack or ambient sound). The workaround is simple - wait a frame:

`function Start() {
yield;
AudioListener.pause = true;
}`

or wait for the fix.

