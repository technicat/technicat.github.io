---
layout: post
title: My First Unity Editor Script
date: '2012-05-14T13:56:34-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515860051/my-first-unity-editor-script
---
I’ve avoided messing with Unity Editor scripts until now, reasoning that I should be spending my time on using Unity, not programming it. But recently I got tired of going through the multistep process of selecting a game object, clicking on its mesh in the inspector, then clicking on that mesh in the Project pane, just to see the mesh properties. So I wrote this little menu item that just lets me select the game object, invoke the menu item (right-click would be even better) and then debug print the information in the console pane (there’s another example in the Unify wiki that displays similar info in a popup window). So here’s my first Unity Editor script (if you want to try it out, put it in a Javascript file and place it under the Editor folder then wait for a while for the menu to show up in the menubar, Refresh the Editor folder if necessary).

`
@MenuItem ("Technicat/Mesh Info")
static function MeshInfo() {
if (Selection.activeGameObject !=null) {
var mf:MeshFilter = Selection.activeGameObject.GetComponent(MeshFilter);
var sm:Mesh = mf.sharedMesh;
if (mf == null) {
Debug.Log(Selection.activeGameObject.name+" No mesh");
} else {
Debug.Log("shader: "+Selection.activeGameObject.renderer.sharedMaterial.shader.name+" normals: "+sm.normals.length+" tangents: "+sm.tangents.length+" colors: "+sm.colors.length+" uv: "+sm.uv.length+" uv2: "+sm.uv2.length);
}
}
}`

Now I’m thinking for all those people who aren’t sure how to get started in programming, this isn’t a bad way. You can start off with simple scripts, get instant results, and learn about the API and the data structures (in this case, what’s in a mesh).

