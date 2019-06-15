---
layout: post
title: Cleaning out a Unity Build with an Editor Script
date: '2013-04-06T04:51:34-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612473706/cleaning-out-a-unity-build-with-an-editor-script
---
I got tired of rooting around in the Mac Finder every time I wanted to remove that last Unity build, so I made simple Editor window that displays the build path and a button to delete it.

`
public class Build : EditorWindow {`

[MenuItem (“FuguGames/Build”)]  
 static void Init() {  
 EditorWindow win = EditorWindow.GetWindow(typeof(Build));  
 }

public void OnGUI() {  
 string path = EditorUserBuildSettings.GetBuildLocation(EditorUserBuildSettings.activeBuildTarget);  
 EditorGUILayout.LabelField(path);   
 if (GUILayout.Button(“Delete Build”)) {  
 FileUtil.DeleteFileOrDirectory(path);  
 }  
 }  
}

