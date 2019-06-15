---
layout: post
title: Custom UINavigationBar Crash
date: '2015-05-12T13:31:58-07:00'
tags:
- ios
- xamarin
- crash
tumblr_url: https://fugugames.tumblr.com/post/118792370651/custom-uinavigationbar-crash
---
Finally figured out why one of my Xamarin apps was crashing in iOS 8.3. Subclassing UINavigationBar and adding a component via the Draw method, as demonstrated in this Xamarin guide snippet, does not work in iOS 8.3. Moving the AddSubview call to the constructor avoids the problem.

public override void Draw (RectangleF rect)  
​ &nbsp; &nbsp;{  
​​ &nbsp; &nbsp; &nbsp; &nbsp;base.Draw (rect);  
 &nbsp; &nbsp; &nbsp; &nbsp;TintColor = UIColor.Purple;  
​​ &nbsp; &nbsp; &nbsp; &nbsp;AddSubview (iv);  
​ &nbsp; &nbsp;}

