---
layout: post
title: SetActiveRecursively
date: '2012-11-21T13:46:07-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612453811/setactiverecursively
---
To use the new SetActive setup in Unity 4, I had to take a lot of my GameObject trees that were a mix of active and inactive objects and make them fully active, with just the root object (or the object under the root object) as the “toggle” object. Since the Editor no longer offers to recursively apply a change to the (local) active state, I wrote a little Editor script:

`
@MenuItem ("FuguGames/ActivateRecursively")
static function ActivateRecursively() {
	if (Selection.activeGameObject !=null) {
		SetActiveRecursively(Selection.activeGameObject,true);
	}
}`

@MenuItem (“FuguGames/DeactivateRecursively”)  
static function DectivateRecursively() {  
 if (Selection.activeGameObject !=null) {  
 SetActiveRecursively(Selection.activeGameObject,false);  
 }  
}

static function SetActiveRecursively(obj:GameObject,val:boolean) {  
 obj.SetActive(val);  
 for (var i:int=0; i\<obj.transform.GetChildCount(); ++i) {  
 SetActiveRecursively(obj.transform.GetChild(i).gameObject,val);  
 }  
  
}

