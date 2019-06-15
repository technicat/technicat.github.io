---
layout: post
title: Finger Gestures
date: '2012-05-21T16:38:06-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515861706/finger-gestures
---
I guess sales really work. I bought the Finger Gestures package during the Unity Asset Store sale, figuring I was going to buy it eventually, anyway. I just got around to trying it out, on my [Elektra Dance](http://itunes.apple.com/us/app/elektra-dance/id298043398) app (updated on Android, we’ll see if Apple takes it), which has been getting by with the original standard assets MouseOrbit script for camera control. It works, but not quite right.

So I installed Finger Gestures, dragged the initializer prefab into the scene, and just added callbacks for finger down/up/move to the MouseOrbit script (the first few lines are in the Start function, registering the callbacks), and using the “delta” values in LateUpdate instead of the Input values that worked with the mouse. The new behavior is actually a bit fancier - since I don’t reset the delta values in the finger up callback, when you release after a swipe, the camera keeps orbiting, giving you a swipe and spin effect. It could use some refinement, as when you swipe with multiple fingers it goes crazy, but I kind of like the resulting manic disco dancing.

In this case, it probably wouldn’t have been difficult to accomplish the same thing accessing Unity’s Input.touches directly, but then you end up trying to implement a state machine inside an input detection loop. With callbacks like this, it’s simpler and clearer. What I’d really like to make use of is the rotation gesture detection. Maybe a gymnastics app?

FingerGestures.OnFingerDown += OnFingerDown;  
FingerGestures.OnFingerUp += OnFingerUp;  
FingerGestures.OnFingerMove += OnFingerMove;  
}

private var lastpos:Vector2;  
private var finger:int=-1;

function OnFingerDown(index:int, pos:Vector2) {  
lastpos = pos;  
deltax = 0;  
deltay=0;  
finger = index;  
}

function OnFingerUp(index:int, pos:Vector2) {  
lastpos = pos;  
finger = -1;  
// deltax = 0;  
// deltay=0;  
}

private var deltax:float = 0;  
private var deltay:float = 0;

function OnFingerMove (index:int, pos:Vector2) {  
if (finger == index) {  
deltax = pos.x-lastpos.x;  
deltay = pos.y-lastpos.y;  
lastpos = pos;  
}  
}

function LateUpdate() {  
if (target) {  
x += deltax \* xSpeed \* 0.02;  
y -= deltay \* ySpeed \* 0.02;

