---
layout: post
title: Demystifying SetActive
date: '2012-11-27T17:49:19-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612454696/demystifying-setactive
---
Unity 4 introduces one API change that seems to cause a lot of confusion - deprecating the GameObject .active property and the SetActiveRecursively function in favor of the properties .activeSelf and .activeInHierarchy and the function SetActive.

It’s not really that complicated. Instead of just a single active state, each GameObject has a locally active state and a globally active state, where the latter is “really” active, equivalent to what active meant in Unity 3 - the GameObject components are effectively disabled and most script callbacks don’t run (and the GameObject is invisible to the Find functions, which is not so convenient)

It’s just like how transforms work. Each GameObject has a local transform, and the global transform which is a function of the local transform and its parent’s global transform, which in turn is a function of its local transform and its parents global transform…

This is a lot easier to wrap your head around if you’re familiar with recursive definitions and implementing them with recursive functions. Here’s how .activeInHierarchy might be implemented in C#:

`
public bool activeInHierarchy {
 get { if (transform.parent) return activeSelf && transform.parent.gameObject.activeInHierarchy else return activeSelf }
}`

To tell you the truth, a lot of this confusion probably arises from the API. SetActive and .activeSelf active are opposite sites of the same coin, where SetActive is the writer and .activeSelf is the reader. It would have been better to have SetActive/GetActive or make .activeSelf a writable/readable property. Better yet, it would have been more consistent and clearer to follow the transform conventions - just like .localPosition and .position, it would have been better to have .localActive and .active.

Anyway, now you should remember that you should refer to .activeInHierarchy where before you read the .active property, and that this “really” active state depends on .activeSelf being true all the way up the parent hierarchy. So in general, you’ll want all GameObjects set to have .activeSelf true, and anytime you want to deactivate a hierarchy of GameObjects, call SetActive(false) on the root of that hierarchy.

In the Editor, clicking on the active checkbox on the GameObject is equivalent to calling SetActive, and the resulting grayed and non-grayed display of the GameObjects indicates their .activeInHierarchy values. So you can experiment by clicking on the checkboxes to get a feel for how it works.

Unity no longer prompts to recursively apply the new active checkbox setting to all of a GameObject’s children, probably because it’s considered not so useful with the new .activeSelf/.activeInHierarchy behavior. Still, when adjusting scenes for Unity 4, chances are you’ll need to batch activate GameObjects. It’s not difficult to write an Editor script for this - in fact, it’s a good exercise in getting to know this API. Check this blog two entries ago for the source.

You might be wondering what’s the point of this change. I think Unity introduced it for Mechanim, but it’s not hard to think of a simple example where it’s helpful to maintain local active state, say a character with a weapon - you could make the weapon appear/disappear by calling SetActive on it, and if you make the character appear/disappear by calling SetActive on its root GameObject, you don’t have to worry about separately tracking the weapon’s active state, since you don’t have to call SetActiveRecursively like you used to. After upgrading all my code to Unity 4, I find this change actually simplifies things. I think the API could be clearer, but I guess this is it until Unity 5.

