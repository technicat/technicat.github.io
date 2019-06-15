---
layout: post
title: Aquamacs and Unity
date: '2010-01-22T03:33:08-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318417876/aquamacs-and-unity
---
I’m a long-time emacs user (beginning with Zmacs on the Symbolics Lisp Machines) and I’m still holding out, using [XEmacs](http://xemacs.org/) on Windows and [Aquamac](http://aquamacs.org/)s on MacOSX. But with Unity, I haven’t tried changing the default editor, largely out of apathy, and also Unitron is adequate and has a nice auto-coloring feature for Unity functions.

However, one of the “Google Friday” projects at Unity is an [Emacs mode for Unity Javascript](http://blogs.unity3d.com/2010/01/15/emacs-mode-for-unity-javascript/), so I just had to try it out. First, I specified Aquamacs as my Unity editor:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/unityemacs.png "unityemacs")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/unityemacs.png)

Then I downloaded the elisp file from the blog article and placed it in my user Library/Preferences directory for Aquamacs.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/aquamacsprefs.png "aquamacsprefs")](http://itshardtofondlepenguins.com/wp-content/uploads/2010/01/aquamacsprefs.png)

Finally, I placed the loading code specified in the blog article into the Preferences.el file (shown in the same directory above). So far, looks good!

