---
layout: post
title: Converting an Animation to iTween
date: '2010-11-17T02:30:28-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411984346/converting-an-animation-to-itween
---
I started converting some of my code that use the Unity animation functions to iTween. For example, here’s the original code that sweeps the “Second Ball!” text onto the screen:

    private var ycurve:AnimationCurve; function Awake () { ycurve = AnimationCurve.Linear(0, transform.localPosition.y, animTime, transform.localPosition.y); AddStartClip(); } function AddStartClip() { var curve = AnimationCurve.EaseInOut(startTime, start, startTime+animTime, transform.localPosition.x); var clip = new AnimationClip(); clip.SetCurve("", Transform, "m\_LocalPosition.x", curve); clip.SetCurve("", Transform, "m\_LocalPosition.y", ycurve); animation.AddClip(clip, animStart); } function Play() { animation.PlayQueued(animStart); }

and the current version:

    function Play() { iTween.MoveTo(gameObject,{"x":0,"time":0.3,"easetype":iTween.EaseType.easeOutQuad}); }

I’d like to think a bunch of conversions like this might help my level start time on the iPhone, but in any case, it sure is a lot more succinct. And there are many more ease-in/out options.