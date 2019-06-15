---
layout: post
title: Some Screenscraping Code
date: '2013-07-15T16:49:14-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110612490736/some-screenscraping-code
---
This is a first - I actually removed an app from sale last week, WordsEye Feature, because the WordsEye site is undergoing some remodeling (the $100k in seed funding they won in an entrepreneurship contest probably has something to do with it). This demonstrates the problem with depending on someone else’s site for your app content and also the problem with screenscraping the content, which is pretty much the least robust approach to accessing web data. I could have tried updating my code, but I’d rather wait for a WordsEye API. In the meantime, here’s what some Unity screenscraping code looks like - it’s not that complicated, the tricky part is getting the regular expressions right. And screenscrape responsibly! (I made this app with permission).

    function Refresh() { // Start a download of the given URL var www : WWW = new WWW (url); // Wait for download to complete yield www; if ([www.error](http://www.error) != null) { SetTitleText([www.error](http://www.error)); } else { var match = regexp.Match([www.text](http://www.text)); var text = match.Groups[4].Value; SetScrollText(text); var title = match.Groups[1].Value; var author = match.Groups[2].Value; SetTitleText("Loading..."); var imageurl = match.Groups[3].Value; var imagewww : WWW = new WWW ("http://wordseye.com"+imageurl); // Wait for download to complete yield imagewww; if (imagewww.error != null) { SetTitleText("Error loading "+title+"n"+imagewww.error); } else { SetTitleText(title+"n"+author); imagewww.LoadImageIntoTexture(render.guiTexture.texture); } } lastdisplay = Time.time; [www.Dispose](http://www.Dispose)(); if (imagewww != null) { imagewww.Dispose(); } }
