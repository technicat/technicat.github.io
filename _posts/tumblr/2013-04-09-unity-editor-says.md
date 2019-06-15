---
layout: post
title: Unity Editor Says...
date: '2013-04-09T17:46:59-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612474941/unity-editor-says
---
Unity Editor scripting is my new diversion. Here’s a script that brings up a window with a text area and button - type some text and hit the button to run the Mac speech synthesizer. Basically, it’s the same as bringing up the Terminal and typing “say”. But this is in the Unity Editor, so it’s cooler. I think I cribbed the shell function from the Unity wiki a long, long time ago.

`
using UnityEngine;
using System.Collections;
using UnityEditor;`

using System.Diagnostics;

namespace Fugu {

public class Say : EditorWindow {

[MenuItem (“FuguGames/Say”)]  
 static void Init() {  
 EditorWindow.GetWindow(typeof(Say));  
 }  
  
 private string something = “”;

public void OnGUI() {

something = EditorGUILayout.TextArea(something);   
 if (GUILayout.Button(“Say it”)) {  
 say(something);  
 }  
 }  
  
 // todo - put this in another script  
 static void say(string text) {  
 shell(“/usr/bin/say”,text);  
 }  
  
 static Process shell(string filename, string arguments) {  
 var p = new Process();  
 p.StartInfo.Arguments = arguments;  
 p.StartInfo.CreateNoWindow = true;  
 p.StartInfo.UseShellExecute = false;  
 p.StartInfo.RedirectStandardOutput = true;  
 p.StartInfo.RedirectStandardInput = true;  
 p.StartInfo.RedirectStandardError = true;  
 p.StartInfo.FileName = filename;  
 p.Start();  
 return p;  
}  
}  
}

