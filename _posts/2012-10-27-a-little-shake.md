---
layout: post
title: A Little Shake
date: '2012-10-27T14:04:12-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612449126/a-little-shake
---
Here’s how I test for a device shake in Unity (shakeThreshold is typically around 5). It’s not exact, but it’s concise:

`if (Input.acceleration.sqrMagnitude>shakeThreshold) {}`

