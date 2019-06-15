---
layout: post
title: Git->Mercurial Quick Tip
date: '2014-08-31T15:57:58-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110698055711/git-mercurial-quick-tip
---
I use github for my public projects and for my private projects on bitbucket, I could use git, but just for the sake of trying something different, at the risk of making things more difficult for myself, I use mercurial. Actually, since I use the Sourcetree GUI for bitbucket, it hasn’t really mattered so far, except the default syntax for ignore files is different. But here’s a quick tip: just add “syntax: glob” to the .gitignore file (and rename it to .hgignore), and you’re fine. For example here’s the line added to the .gitignore taken from one of the Xamarin repos on github to make it usable with mercurial:

    syntax: glob \*.pidb \*.userprefs \*.swp \*.DS\_Store \*.nib obj/\* bin/\* \*/bin/\* \*/obj/\* \*/\*/bin/\* \*/\*/obj/\*

