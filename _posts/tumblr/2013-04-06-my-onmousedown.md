---
layout: post
title: My OnMouseDown
date: '2013-04-06T21:44:26-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612474146/my-onmousedown
---
I used to roll my own OnMouseDown on Unity mobile, so that my front end menu screens in HyperBowl worked the same on desktop, webplayer and mobile. I removed that code after Unity implemented OnMouseDown themselves. But those warnings about how OnMouseDown may impact performance are beginning to worry me, so I’m renaming my OnMouseDown callbacks to avoid the warning (and the possible slowdown, wherever it may be), and I brought back my OnMouseDown issuing code. It’s a bit cleaner, and now in C#.

Attach it to a Camera, and it will perform raycasts to the Camera’s visible layers, and then trigger the callback, which I’ve hardcoded to the name OnButtonDown (along with the raycast distance - both could be public properties), since I’m just using it for the front end menu buttons in HyperBowl. So the raycasts are just limited to that particular camera, that camera’s visible layers, and that particular scene. And I check the timeScale to see if the game is pause, which in HyperBowl means the pause menu is up and front end interface should be frozen.

`
public class ButtonDown : MonoBehaviour {
#if UNITY_IPHONE || UNITY_ANDROID		
	private int layermask = 0;
	const float distance = 150.0f;`

void Awake() {  
 layermask=camera.cullingMask;  
 }  
  
 void Update () {  
 if (Time.timeScale !=0 ) {  
 RaycastHit hit;  
 for (int i = 0; i \< Input.touchCount; ++i) {  
 Touch touch = Input.GetTouch(i);  
 if (touch.phase == TouchPhase.Began) {  
 // Construct a ray from the current touch coordinates  
 Ray ray = camera.ScreenPointToRay (touch.position);  
 if (Physics.Raycast (ray,out hit,distance,layermask)) {  
 hit.transform.gameObject.SendMessage(“OnButtonDown”);  
 }  
 }  
 }  
 }  
 }

