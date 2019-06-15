---
layout: post
title: You Want a Cup of BREW or Java?
date: '2011-10-08T21:14:59-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515777806/you-want-a-cup-of-brew-or-java
---
Wow, the last line in this review is really obsolete.

_Originally written on Epinions in July 2003:_

In recent years, products and technologies based on the Java programming language have made software development sound like a trip to Starbucks. Kaffe, Jakarta, JavaBeans…and the list goes on.

Qualcomm has jumped on this caffeine bandwagon with BREW, which stands for Binary Runtime Environment for Wireless. Any number of applications can be developed on BREW, but the hype has been on games as the killer app for cell phones, and this is what Ralph Barbagallo discusses in **Wireless Game Development in C/C++**.

The book begins with a brief overview of the other prominent cell phone gaming platforms - WAP (a standard for web browsing), J2ME (Java on cell phones), iMode (the popular Japanese cell phone network) before introducing BREW, and listing a few BREW-enabled cell phones and example games.

The bulk of the book explores how BREW is used for the major functionality required by games: user interface, bitmap and tiled graphics, storage, audio, and wireless networking. These sections are explained at a programmer level, complete with example code.

Possibly the most useful chapters are on constructing a simple example game, building your own reusable libraries, installing a game on the target hardware, and on the certification and publishing process. There is also a chapter on optimization that has nothing new for an experienced game programmer, but is useful for programmers new to the game development scene.

As the title of the book indicates, BREW programs are written in C or C++ and thus BREW is normally considered a competitor to J2ME (Java 2 Micro Edition), but one appendix discusses the possibility of running J2ME on top of a BREW platform.

The other appendices briefly discuss C++, fixed pointer numbers, the BMP file format and newer versions of BREW. But any programmer not already familiar with these subjects will need much more extensive documentation. Experienced programmers will consider some of the C++ and optimization topics trivial, and a few items not quite right, or at least debatable. For example, Mr. Barbagallo distinguishes between a “library” and “dynamic library”. These days, the former is typically termed a “static library” to make it clear - it’s only old fogey programmers who remember that before dynamically-loaded libraries, all code libraries were statically linked into applications.

Although most of the books is oriented toward programmers, others in the game and cell phone industries will find the introductory chapters and sections on certification/publishing and newer versions of BREW useful. However, the comparison between BREW and J2ME seems to be biased towards BREW and fails to stress the primary potential drawback of BREW - it’s proprietary nature and availability only on Qualcomm hardware. This is an unfortunate omission, since the most important decision in developing a cell phone game these days possibly is in choosing whether to go with BREW or J2ME.

