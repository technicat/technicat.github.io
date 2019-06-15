---
layout: post
title: Unicoding Your Web Page
date: '2011-11-03T17:44:52-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515789866/unicoding-your-web-page
---
One feature I added to my [Fugu Games](http://fugugames.com/) site is the display of a randomly-selected 5-star review from the App Store. But some of the reviews are written with foreign character sets, so I had to Unicodify the page. Really, just two steps:

- use a font that has all the required characters. I picked Lucida Sans Unicode, applied via CSS
.quote { font-family: Lucida Sans Unicode, sans-serif; }
- 

    specify a Unicode-capable character encoding at the top of the HTML file

\<!DOCTYPE HTML PUBLIC “-//W3C//DTD HTML 4.01 Transitional//EN” “http://www.w3.org/TR/html4/loose.dtd”\> \<html\> \<head\> \<META http-equiv=“Content-Type” content=“text/html; charset=UTF-8”\> And now, proper foreign characters show up correctly! (and in this example below, I’m disappointed to see, via google translate, that it’s spam)[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/11/Screen-shot-2011-11-03-at-9.17.28-AM.png "Screen shot 2011-11-03 at 9.17.28 AM")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/11/Screen-shot-2011-11-03-at-9.17.28-AM.png)I feel compelled to elaborate on a point that confuses even experienced software developers - Unicode is not an encoding, at least in terms of how express characters in bytes. Unicode is a mapping of characters to numbers. UTF-8 and UTF-16 are variable-byte encodings that can represent all Unicode characters. The 8 in UTF-8 doesn’t mean that it’s always just one byte - one byte is the minimum, equivalent to anything that can be represented by ASCII, and the high bit indicates whether or not more bytes will follow to represent the character in question. I’ve seen a lot of confusion with Java, which internally uses Unicode and has a lot of nice facilities for reading and writing characters in different formats, but engineers often knock themselves out writing their own character encoding/decoding routines.
