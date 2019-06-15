---
layout: post
title: Quick-Open a Unity Scene
date: '2013-06-07T22:07:23-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612482116/quick-open-a-unity-scene
---
One thing that always seems to take more work than it should in Unity is switching scenes. The Open Scene item in the File menu is out of the question, but rooting around for the scene in the Project View often isn’t much faster. Here’s OnGUI function that you can place inside an EditorWindow subclass in an Editor script. It will list every scene that’s in the BuildSettings window along with an Open button to open that scene.

`
public void OnGUI() {
foreach (EditorBuildSettingsScene scene in EditorBuildSettings.scenes) {
EditorGUILayout.LabelField(scene.path);
if (GUILayout.Button("Open")) {
EditorApplication.OpenScene(scene.path);
}
}`

}

