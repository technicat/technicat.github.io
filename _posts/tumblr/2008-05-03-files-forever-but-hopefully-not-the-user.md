---
layout: post
title: Files Forever (but hopefully not the user interface)
date: '2008-05-03T04:01:58-07:00'
tags:
- Dreamhost
- GUI
- user interface
- web design
tumblr_url: https://fugugames.tumblr.com/post/110242896796/files-forever-but-hopefully-not-the-user
---
When a fellow [Unity](http://www.unity3d.com/) developer inquired about licensing the source code for my [FuguMaze](http://www.apple.com/downloads/dashboard/games/fugumaze.html) widget, I decided to try out Dreamhost’s Files Forever service. Once I’ve uploaded the file I want to sell, I send the prospective buyer this [link](https://files.dreamhost.com/58179/fugumaze.zip), which leads the buyer to this page:

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-1.png "picture-1")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-1.png)

This is a terrible web interface. <!--more-->It’s really not obvious what to do, and what seems obvious doesn’t work: if you what looks like a download icon, nothing happens. And if you experiment, you’ll get yelled at. For example, I decided to hit the Share button.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-2.png "picture-2")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-2.png)

Now, that’s not very nice. It does say “please” fix the error, but in that same message it could state what the error is and how to fix it. It does say the address field is blank by the address field, but that is stating the obvious and doesn’t explain exactly what’s supposed to be in there and why it’s required - I’m going to guess that it’s the email address of the person I want to share the file with, but does that person already need to be a Files Forever member? Why not explain it here and not make me guess? And what’s with the error message in the login box? How about one, clear, error message?

And it just seems weird that I can choose to share a file without having selected it via the download/add-to-cart option at top. How can I share it without buying it, first? Oh, buy clicking Share I did add-to-cart even though it gave me an error page. This is made known to me because I decided to hold off on that share thing for now and just click Add to Cart.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-3.png "picture-3")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-3.png)

I might proceed to checkout, but say I’m a bit confused now, and decide to start over by removing the item from the cart.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-6.png "picture-6")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-6.png)

This is a waste of a page, entirely dedicated to telling me that the last button click worked, and now I have to click on the back link to proceed. It could have just refreshed the main page with the cart contents updated and perhaps a success message in the same place where we saw the error message before.

OK, I’ve just started this process and now I’m already getting annoyed. But let’s go to checkout.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-4.png "picture-4")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-4.png)

One quibble here. To do anything with Files Forever, you have to have a files forever account - that’s what the email address and password is for. To make that clear, why not put that at the beginning of the process instead of the end?

The bigger problem happens after you complete the purchase. You’ll get an email with the same URL and thus the same initial screen as you used to start the purchase process. If you read the email very thoroughly and stare hard at the screen, you’ll figure out that you have to login with the email address and password you selected. If you’re like my first customer, you’ll see that same screen telling you have to Add to Cart to download the file, you’ll click on that, and then you’ll feel like you’ve done this before.

But if you do figure out you have to log in, you’ll start to see some action.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-8.png "picture-8")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-8.png)

If you notice the download icon has changed color, you may discover that that download icon is now clickable - wow, it really is a download icon after all! Now, why does it say “but you already own it”. Of course I do, that’s why I logged in to download it. At this point, I’m not too confused, but apparently the code is. This seems like the programmer tried to wedge everything together in the name of reusability. Purchasing files and downloading files that you’ve purchased are two separate tasks and take place at different times. The web pages in these different phases should look different and be tailored to each process, rather than a one-page-fits-all approach.

To cap off the theme of bad programming, when you log out, you get some nice gibberish which appears to be a programming error.

[![](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-11.png "picture-11")](http://itshardtofondlepenguins.com/wp-content/uploads/2008/05/picture-11.png)

Who is this user “-1” who has 10 files, and why does my file now show up in his shopping cart?

The explanatory text in the main pane is because I decided to RTFM in the end by clicking on the “What is this?” label at the top of the page. It’s not that helpful, and could in fact be crammed into the space taken up by the huge Files Forever and Dreamhost banners (and the Best Web Hosting Ever link is really unnecessary - that page just a marketing page for Dreamhost and doesn’t even mention Files Forever, and at worst, gives the impression that you have to be a Dreamhost customer to use Files Forever). The link for performing a practice purchase and download - no one’s going to do that, if you have to do that, your process is way to complicated, and if you really want people to do that anyway, that link should be on the main page, not hidden inside “What is this?”

I believe Files Forever is in beta (not obvious on the Files Forever pages, but mentioned in the Dreamhost wiki, I think), but for a long time. I don’t think it’s getting out.

