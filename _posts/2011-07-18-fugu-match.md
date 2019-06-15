---
layout: post
title: Fugu Match
date: '2011-07-18T05:14:33-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515732176/fugu-match
---
I’ve been thinking for a while I should dig into the [Unity example projects](http://unity3d.com/support/resources/example-projects/iphone-examples) and try to publish my own variations of them. Partly because I need to really muck around in a project to understand how it works, partly because running a one-person shop I should really try to be efficient and reuse as much as I can, and partly because I just want to get my money’s worth.

So finally, months after a potential client/partner approached me about making a memory match game, I took a look at the Unity iPhone match game example. I figured at minimum I could revise the graphics and improve the game flow (the demo doesn’t have an option to restart the game).

This is the part where you say offhandedly, “that should be easy”. But of course, it was a bit trickier than I anticipated. There are basically three important scripts in that demo, a script attached to the card prefabs that perform the initial reveal animation, a script that generates all the visible cards, and the script that runs the rest of the game.

To get the game to restart upon a screen tap at the end of the game, detecting the tap was simple, I just added a call to Input.OnMouseDown, which is an easy way to check for taps without actually writing mobile-specific code (and it has the advantage of letting you test in the Editor with a mouse click), but to get it to start the game over I ended up merging the card-instantiation and game-loop script and reorganizing the result into a state machine using coroutines as the states so I could easily transition from the end to the beginning.

But then I had to decide to reuse the initially generated cards or destroy them and start completely over. The former sounds like the obvious choice, but the cards are actually generated from a set of prefab cards in the scene, which are destroyed after they are copied, and the logic for randomizing the cards is intertwined with their generation. So the most expedient path to getting a restartable game was to just to completely start over. This, however, meant not destroying the original prefab cards since we’ll need them for the next game restart, and then now we find out the Start function that runs the reveal animation in the cards will break in the original prefab cards because they apparently never ran before they were destroyed. Again, expedient measure - I tweaked those functions so they don’t break (they referenced some fake shadow geometry that are added to the visible cards but not the original prefabs).

And finally, even changing the graphics was not as straightforward as I assumed. I replaced the background with some built-in water, no problem. Replacing the back of the cards with a new texture was easy. But the individual images used for matching actually are not individual texures, but all glommed onto the same texture, from which I deduced the card geometry had different texture coordinates for each card. Which provided some explanation for why there was a different prefab defined for each possible card. So I left that alone for now, since I didn’t feel like coming up with exactly the same number of images and then combining them into one texture.

Also, after testing it a bit, I realized I had no idea how the scoring worked, so I removed it as non-obvious and just left the timer countdown. And, since I don’t feel the app at this point merits charging, but hell if I’m going to release it without trying to get some revenue, so I moved the timer to the bottom of the screen so I’d have room for banner ads at top. And in a last bid to get an original look, I replaced the font and replaced the game-over/you-win graphics with text. Even that required a little tweaking of the code - those variables referenced GUITextures, so I made them GameObjects instead, which will work for anything.

Finally, here’s the result, [Fugu Match](https://market.android.com/details?id=com.technicat.fugumatch) on the Android Market:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2011/07/device.png "device")](http://itshardtofondlepenguins.com/wp-content/uploads/2011/07/device.png)

In the future, I’d like to replace the animation with iTween, invoke another reveal at game end so you can see what you failed to remember, reintroduce a scoring system perhaps, maybe shake to scramble the cards, integrate with Game Center on iOS, revise the card face graphics (or let the user add them). In my first-year theoretical calculus class, I failed to remember an of the theory, but I do remember the instructor saying you figure out the proof in a messy fashion, then you erase the board and rewrite it as if you knew where you were going all along. You could say the same about code.
