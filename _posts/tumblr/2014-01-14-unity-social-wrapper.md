---
layout: post
title: Unity Social Wrapper
date: '2014-01-14T13:27:50-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612516226/unity-social-wrapper
---
Here are my wrapper functions for Unity’s GameCenter API. They take care of things like logging debug info (if activated by a preprocessor definition) and smooth out the inconsistency between the leaderboard and achievement parameter order (Social.ReportProgress takes the achievement name first and progress second, while Social.ReportScore takes the score first and the name second). I wrote this when I switched from the Prime31 plugin to the Unity API, but I plan to add the Prime31 option back in like I did with my iAd script.

    using UnityEngine; using UnityEngine.SocialPlatforms.GameCenter; namespace Fugu { sealed public class GameCenter : MonoBehaviour { public bool showAchievementBanners = true; // Use this for initialization void Start () { #if UNITY\_IPHONE Social.localUser.Authenticate ( success =\> { if (success && showAchievementBanners) { GameCenterPlatform.ShowDefaultAchievementCompletionBanner(showAchievementBanners); Debug.Log ("Authenticated "+Social.localUser.userName); } else { Debug.Log ("Failed to authenticate "+Social.localUser.userName); } } ); #endif } static public void Achievement(string name) { Achievement(name,100.0d); } static public void Achievement(string name,double score) { #if UNITY\_IPHONE if (Social.localUser.authenticated) { Social.ReportProgress(name,score, success =\> { #if FUGU\_DEBUG if (success) { Debug.Log("Achievement "+name+" reported successfully"); } else { Debug.Log("Failed to report achievement "+name); } #endif }); } #endif } static public void Score(string name,long score) { #if UNITY\_IPHONE if (Social.localUser.authenticated) { Social.ReportScore (score, name, success =\> { #if FUGU\_DEBUG if (success) { Debug.Log("Posted "+score+" on leaderboard "+name); } else { Debug.Log("Failed to post "+score+" on leaderboard "+name); } #endif }); } #endif } } }

