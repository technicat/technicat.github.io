---
layout: post
title: Sharing Unity MenuItem Functions
date: '2012-11-24T00:20:26-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612454211/sharing-unity-menuitem-functions
---
Here’s a little Unity Editor scripting trick. To have menu items enabled/disabled depending on context, you need to declare the menu item a second time with a boolean parameter, followed by the test function. But it’s pretty redundant to write the same function over and over again to check, for example, if a GameObject is selected. Fortunately, you can stack up menu item declarations and have them share one function, like this:

`
@MenuItem ("FuguGames/ActivateRecursively", true)
@MenuItem ("FuguGames/DeactivateRecursively", true)
@MenuItem ("FuguGames/Mesh Info",true)
@MenuItem ("FuguGames/CreateChild",true)
static function ValidateGameObject() {
	return (Selection.activeGameObject !=null);
}`

