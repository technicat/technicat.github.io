---
layout: post
title: Mouse Callbacks with Unity Flash
date: '2012-01-08T14:57:30-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515810641/mouse-callbacks-with-unity-flash
---
One thing missing from the Flash exporter in the Unity 3.5 developer preview is support for the OnMouse callbacks. So, as with Unity iOS and Android, you have to roll your own. Here’s what I coded for the Flash version of [HyperBowl](http://hyperbowl3d.com/) (only for game objects with colliders, not GUIText/Texture):

`
private var layermask:int = 0;`

private var hitobject:GameObject;

function Awake() {layermask=1\<gameObject.layer; }

function Update () {  
var hit : RaycastHit;  
var ray = camera.ScreenPointToRay (Input.mousePosition);  
if (Physics.Raycast (ray,hit,150,layermask)) {  
if (Input.GetMouseButtonDown(0)) {  
hit.transform.gameObject.SendMessage(“OnMouseDown”,SendMessageOptions.DontRequireReceiver);  
} else {  
if (hitobject != hit.transform.gameObject) {  
if (hitobject != null) {  
hitobject.SendMessage(“OnMouseExit”,SendMessageOptions.DontRequireReceiver);  
}  
hitobject = hit.transform.gameObject;  
hitobject.SendMessage(“OnMouseEnter”,SendMessageOptions.DontRequireReceiver);  
}  
}  
}  
}

