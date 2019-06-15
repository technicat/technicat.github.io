---
layout: post
title: Look at My Mouse
date: '2011-12-18T12:19:17-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515801661/look-at-my-mouse
---
Here’s a little code snippet I used in my [old Fugu Games site](http://fugugames.com/indexold.html) to have objects constantly look toward the mouse cursor position - I just thought it was cute to have the the little Fugu balls doing that. Just attach this script to anything that you want to behave that way, and adjust that hardcoded z value of the point you’re converting from screen to world coordinates.

`function Update() {
transform.LookAt(Camera.main.ScreenToWorldPoint(Vector3(Input.mousePosition.x,Input.mousePosition.y,5)));
}`

