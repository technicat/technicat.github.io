---
layout: post
title: Making iPhone Apps on the Web
date: '2010-11-02T14:28:44-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411979426/making-iphone-apps-on-the-web
---
Last week I tried out [AppMakr](http://appmakr.com/), a web site that allows you to create an iPhone app online. Before you get too excited, these apps are simply collections of one or more RSS feeds, so you’re not going to make any games with this system, but it is suited to creating app versions of web sites or aggregations of feeds.

Putting an app together with AppMakr is really easy if you have suitable feeds (alas, Facebook pages are uncooperative - AppMakr has instructions on how to wrangle them with Yahoo Pipes). You can pay them to publish your app, or you can download test and distribution builds and use your own Apple account, which is free and painful, since you can’t use existing certificates - AppMakr requires you to create new ad-hoc (for testing on your own device) and distribution certificates/mobileprovisions for each app. I assume the process for updates is easier. AppMakr will also refuse to complete the build/publish process if it doesn’t satisfy their criteria, which attempt to anticipate whether Apple will accept or reject the submission. One criterion includes the popularity of the app web site, which seems to limit the target audience to online magazines with a really low iPhone development budget.

Although the parts involving iTunesConnect are arduous, AppMakr has excellent step-by-step instructions and corresponding YouTube videos, which are worth viewing even if you just want to get an idea what’s involved in preparing any app for publication.

[AppCookr](http://appcookr.com/) is a newer and similar service, but also with Android support. Unfortunately, you have to choose one or the other when you create an app, so you can’t just create an app and publish for both. Interestingly, AppCookr’s web-based iPhone simulator uses Silverlight. Overall the site doesn’t look as polished as AppMakr (some English mistakes, not as much help), but besides the Android support, AppCookr has some other features, like a web-page display, so next time I have a suitable app (or if I want dip my toe into Android development), I might give AppCookr a try.

