---
layout: post
title: A Better Delete-Build Window
date: '2013-07-04T23:35:34-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612486316/a-better-delete-build-window
---
A while ago I posted a simple Unity Editor script that provides a convenient button to delete a recent build. Since then I’ve consolidated my projects so they’re multiplatform, so the script now lists all the build targets that have been used in the project. And there are refinements such as marking the currently active build target and only displaying the Delete button if the build file (or folder) exists.[![Screen Shot 2013-07-04 at 7.30.21 PM](http://itshardtofondlepenguins.com/wp-content/uploads/2013/07/Screen-Shot-2013-07-04-at-7.30.21-PM.png)](http://itshardtofondlepenguins.com/wp-content/uploads/2013/07/Screen-Shot-2013-07-04-at-7.30.21-PM.png)Place this code inside a C# class that extends EditorWindow:

    [MenuItem ("FuguGames/Builds")] static void Init() { EditorWindow.GetWindow(typeof(Build)); } public void OnGUI() { LayoutTarget(BuildTarget.iPhone); LayoutTarget(BuildTarget.Android); LayoutTarget(BuildTarget.WebPlayer); LayoutTarget(BuildTarget.WebPlayerStreamed); LayoutTarget(BuildTarget.StandaloneWindows); } private void LayoutTarget(BuildTarget target) { string path = EditorUserBuildSettings.GetBuildLocation(target); if (!System.String.IsNullOrEmpty(path)) { EditorGUILayout.BeginHorizontal(); string name = target.ToString(); if (EditorUserBuildSettings.activeBuildTarget == target) { name = name + " (current)"; }; EditorGUILayout.LabelField(name); if (System.IO.File.Exists(path) && GUILayout.Button("Delete Build")) { FileUtil.DeleteFileOrDirectory(path); } EditorGUILayout.EndHorizontal(); EditorGUILayout.LabelField(path); } }

