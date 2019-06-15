---
layout: post
title: How to Move Kinematic Rigidbodies
date: '2012-07-25T15:25:36-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612428951/how-to-move-kinematic-rigidbodies
---
You’ll often hear or read the advice that you should never move static colliders in Unity - always add kinematic rigidbodies to those objects. Less often, you’ll hear or read that you should use the Rigidbody move and rotate functions instead of modifying the object transform, so that friction is properly taken into account. What isn’t quite documented as far as I can tell is, once you go with a kinematic rigidbody, modifying its transform is actually slower, a lot slower, than moving a static collider. This I’ve found from experience.

So, bottom line, if you’re moving a collider, you should use a kinematic rigidbody, but only if you just manipulate it through the rigibody, not through the object transform.
