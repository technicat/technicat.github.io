---
layout: post
title: WordsEye Feature 1.1
date: '2009-07-25T15:28:08-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110318368581/wordseye-feature-11
---
Finally, I got the last remaining app updated to iPhone OS 3.0, [WordsEye Feature](http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=305827351&mt=8). And by update, I mean, not crashing. This update does have new functionality - now it displays the scene title and author, which should be gratifying at least to the author (I certainly enjoy seeing my own name on these things)[![Picture 6](http://itshardtofondlepenguins.com/wp-content/uploads/2009/07/Picture-6.png "Picture 6")](http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=305827351&mt=8)The Mac [widget](http://www.apple.com/downloads/dashboard/justforfun/wordseyefeature.html) is also updated. Like most of my other apps, this started out as a this-could-be-neat idea for a widget, but unlike the other apps, I released it for the iPhone first and it had more of a start-and-stop history:

1. Thought a Mac widget that retrieves and displays the “featured” scenes from the [WordsEye](http://wordseye.com/) server in a slideshow manner would look cool.
2. Talked it over with my friends at [Semantic Light](http://semanticlight.com/), who run the WordsEye site, to make sure they’re OK with it.
3. Gave it a try, started turning into a lot of work, decided it wasn’t a high priority since I wasn’t going to charge for it, and the built-in audience for WordsEye isn’t huge (but who knows, maybe it’ll attract new WordsEye users)
4. A year later, after starting iPhone app development, thought, hey, that WordsEye viewer would look cool on the iPhone screen (the images almost match the screen size)
5. Went back to the code, got it working, tried it on the iPhone, and sitting on the couch flipping through the images while watching bad TV, thought, hey, this does look cool.
6. A few months later, finally got around to that original widget.
The sharp-eyed WordsEye user might notice that the images in this latest iPhone release are cropped on the top and right sides. The original WordsEye images are slightly larger than the iPhone screen - the previous version scaled the images to fit, but the new image-downloading code in this version apparently has a bug that prevents it (not evident in the widget). The scaling does change the aspect ratio slightly, so one could argue that cropping is better (or perhaps scaling to fit the screen and then adding a border to maintain the aspect ratio, like on wide TV screens, but that just wastes the limited display area of the iPhone screen). I think the scaling looks better, but rather than add some special-case workaround code this time around, I’ll just wait for the next Unity engine update.
