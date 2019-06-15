---
layout: post
title: Vectors on YouTube, or 3D for 3Dummies
date: '2011-12-30T21:02:50-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515805326/vectors-on-youtube-or-3d-for-3dummies
---
There’s a pretty big leap from 2D to 3D game development, not the least of which is the math. In 2D, you can mostly get away with just basic arithmetic and the x,y coordinate system that hopefully we managed to absorb in school (unless you attended Flatland High). But in 3D, you have to deal with, naturally, a 3D coordinate system, where each point is represented by x,y,z coordinates. That sounds like a straightforward extension, but you have to be aware of which way your axes point - Unity uses a [left-handed coordinate system](http://www.evl.uic.edu/ralph/508S98/coordinates.html) and has the Y axis pointing up, while CryEngine uses a right-handed system and has the z axis pointing up.

Once you understand 3D coordinates (and please do, I once worked with an experienced game artist who couldn’t tell me which ways positive X and Z were pointed in the game world!), if you do any type of game programming at all (including scripting), you need to understand vectors. When I watched Despicable Me, I was surprised to hear Vector providing a pretty good definition of his name: “An arrow with direction and magnitude”:

Thus, anything with direction and magnitude can be represented by a vector. Velocity, acceleration, force, light direction, camera direction…vectors that are used solely for directions are often “normalized”, i.e. unit-length.

Vectors are almost as ubiquitous as points, and look a lot like them, but keep in mind the difference between them. Points are just positions. This can be a little confusing since 3D API’s often reuse their Vector data structures to also represent points (Unity is no exception). Unity provides Vector2 for vectors with x, components, Vector3 for x,y,z and Vector4 for x,y,z,w but usually you’ll work with [Vector3](http://unity3d.com/support/documentation/ScriptReference/Vector3.html) (Vector4’s usually come into play when you’re working with matrices). Now, despite what I just said, you can visualize a vector x,y,zas an arrow starting from point 0,0,0 and ending at the point x,y,z and the magnitude of the vector is the length of that arrow (or ray, and raycasting is another use for vectors).

Vectors aren’t that useful unless you can do vector math with them - the important ones are addition, subtraction, scaling, normalization, dot products and cross products. Look at the Unity Script Reference for vectors and you’ll see the corresponding functions. Here’s another YouTube video that explains some of them:

If you find my intro to vectors lacking, keep in mind I barely passed my linear algebra course in college. But hey, we didn’t have YouTube back then!

