---
layout: post
title: Bowling Pin Physics
date: '2013-01-18T04:31:58-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612464466/bowling-pin-physics
---
When you’re playing a game, you take a lot for granted. Take for example the bowling pins in HyperBowl - I spent a lot of time tweaking them to get decent physics behavior (in fact, I made serious error in my first attempt, importing meter-scale models with Unity’s default 0.01 import scale and then trying to compensate by adjusting the Physics Settings, resulting in weebles-wobble-but-they-don’t-fall down pin physics)

Here’s a selected bowling pin:

[![Screen Shot 2013-01-18 at 1.08.08 AM](http://itshardtofondlepenguins.com/wp-content/uploads/2013/01/Screen-Shot-2013-01-18-at-1.08.08-AM1.png)](http://www.fugutalk.com/?attachment_id=5967)

Key things to note: it has a rigidbody, so it will react to collisions and forces, the mass is 1.5kg (rule of thumb, start with realistic values before you try strange ones), the collider is composed of multiple primitive colliders to approximate the pin shape (Unity, or rather PhysX, doesn’t have a cylinder collider so we make do with a box collider on the bottom, a capsule for the neck, and spheres to fill out the rest) - each collider a child of the root pin object, there’s a pinstatus script that checks if a pin has been knocked down (I just check the angle to see if it’s tilted enough), a sound script that plays the pin-to-pin, pin-to-ball or pin-to-ground collision sounds (one subtlety - make sure in pin-to-pin collisions only one pin makes the sound)

Not shown in the picture is the physics material (since it’s attached to the colliders). I set maximum friction because I want the pins to roll, not slide, and fairly high bounciness, since bowling pins are fairly bouncy, and it just looks more fun.

