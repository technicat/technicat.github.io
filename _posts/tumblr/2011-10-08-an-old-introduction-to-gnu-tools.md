---
layout: post
title: An Old Introduction to GNU Tools
date: '2011-10-08T20:50:39-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515772981/an-old-introduction-to-gnu-tools
---
_Originally written on Epinions in January 2004:_

Despite the 1997 publication date, I recently purchased **Programming with GNU Software: Tools from Cygnus Support** because I was in quick need of a reference on using the GNU compiler ( **gcc** ) and debugger ( **gdb** ).

The book fulfilled my requirements handily - the chapters on **gcc** and **gdb** explain how the operation and most common options of those tools. And although the approximately 230-page length of this work is svelte compared to the typical general-programming-in-Unix-or-Linux guide, it turns out to be an excellent introduction to Unix (and by Unix I also mean Linux) systems for programmers. The chapters on getting around in the Unix shells, the **emacs** editor, the **make** system for configuring and invoking builds, source code management with **rcs** , and profiling with **gprof** refer mostly to the toolchain created by the Free Software Foundation (and supported/improved by Cygnus Support which has since been acquired and spun off again by Redhat). But this is also the core development software for Linux and is basically all you need to write, run, and debug a program on Linux.

The inclusion of **rcs** rather than the now ubiquitous **cvs** hints at the age of this work. And considering this book is targeted toward programmers and is not a “dummies” book, it wouldn’t hurt to have a bit more in-depth explanation. For example, the chapter on **emacs** could elaborate on the underlying mechanisms of the editor - syntax and semantics of the **elisp** programming language, the distinction between major and minor editing modes, and customization hooks.

Still, this concise and well-paced guide is a good refresher - I either didn’t know or had forgotten about the emacs **etags** facility (used to track source file locations of code symbols) or subtleties in shell programming (conditionals in shell scripts treat zero instead of non-zero as true, since programs return exit codes of zero to indicate success and non-zero for errors). Many Windows programmers are venturing into Linux waters these days and could use a programmer-friendly introduction such as this. I hope O'Reilly will publish an updated and expanded revision soon.

