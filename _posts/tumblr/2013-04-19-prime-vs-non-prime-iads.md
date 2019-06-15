---
layout: post
title: Prime vs. Non-Prime iAds
date: '2013-04-19T15:50:46-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612475801/prime-vs-non-prime-iads
---
It’s nice to have iAd functionality built into Unity, but the banner ads have long had an unsightly non-refreshing behavior, where the banner turns all white instead of disappearing when it doesn’t have ad content(and yes, I submitted a bug report).

So I’m switching back to the Prime31 iAd plugin, which doesn’t have this problem. Also, the Prime31 version is super easy to use, as evidenced by my banner ad script. One line is required to create the Prime31 ad. All the rest of the script is for the Unity version.

`
public class AdBanner : MonoBehaviour {
	public bool showOnTop = true;
#if FUGU_ADS
#if P31_IAD
	void Start() {
		AdBinding.createAdBanner (!showOnTop);
		}
#else
	private ADBannerView banner = null;
	IEnumerator Start() {
		GameObject.DontDestroyOnLoad(gameObject); // keep ad alive if we load a new scene
		banner = new ADBannerView();
		banner.autoSize = true;
		banner.autoPosition = showOnTop ? ADPosition.Top : ADPosition.Bottom;
		while (!banner.loaded && banner.error == null) {
			yield return null;
		}
		if (banner.error == null) {
			banner.Show();
		} else {
			banner = null;
		}
		}
#endif
#endif`

