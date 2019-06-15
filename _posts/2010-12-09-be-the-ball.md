---
layout: post
title: Be the Ball
date: '2010-12-09T15:48:32-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411991156/be-the-ball
---
Here’s a little Unity script snippet that implements the HyperBowl-style bowling mouse control. This is actually from [FuguBowl](http://fugugames.com/) - the [HyperBowl](http://hyperbowl3d.com/)is more convoluted (possibly unnecessarily) in an attempt to handle more performance variations and platforms.

`
var power = 3.0;
var powerx = 2.0;`

function FixedUpdate () {  
var force:Vector3 = new Vector3(powerx\*Input.GetAxis(“Mouse X”),  
0,  
power\*Input.GetAxis(“Mouse Y”));  
rigidbody.AddForce(force);  
}

