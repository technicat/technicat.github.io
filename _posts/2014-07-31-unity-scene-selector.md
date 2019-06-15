---
layout: post
title: Unity Scene Selector
date: '2014-07-31T02:43:53-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110698049951/unity-scene-selector
---
This week I was showing off the Unity project for HyperBowl, and while I was using my scene-selection Editor script, someone remarked I should put it up on the Asset Store. In fact, I do have it on github (in my FuguEditor repo), but the script is so short it hardly warrants being on the Asset Store, at least not on its own. Here it is - basically, the script just lists and allows you to open all the scenes that also appear in the Build Settings window (and in the same order), which I find a lot more convenient than searching for them in the Project pane. It doesn’t prompt to save, though, so make sure you save the current scene before opening a new one with this script.

    public class SceneSelector : EditorWindow { [MenuItem ("FuguGames/Scene")] static void Init() { EditorWindow.GetWindow(typeof(SceneSelector)); } public void OnGUI() { foreach (EditorBuildSettingsScene scene in EditorBuildSettings.scenes) { EditorGUILayout.BeginHorizontal(); EditorGUILayout.LabelField(scene.path); if (GUILayout.Button("Open")) { EditorApplication.OpenScene(scene.path); } EditorGUILayout.EndHorizontal(); } } }

[![Screen Shot 2014-07-30 at 11.13.44 AM](http://itshardtofondlepenguins.com/wp-content/uploads/2014/07/Screen-Shot-2014-07-30-at-11.13.44-AM.png)](http://itshardtofondlepenguins.com/wp-content/uploads/2014/07/Screen-Shot-2014-07-30-at-11.13.44-AM.png)
