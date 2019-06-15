---
layout: post
title: Battle of the ChatBots
date: '2008-09-27T13:29:09-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110242914486/battle-of-the-chatbots
---
One of my less-smart career decisions was in joining a startup in Venice, CA that aimed to deploy talking 3D characters to field customer support requests. Attempting to beat the Turing Test is a lofty challenge, but after all, I did leave the Bay Area, filled with MBA’s starting B2B ventures, to find something interesting. My mistake was selecting a technology company run by Hollywood producers (didn’t work for Yahoo, either) and not testing the demo myself - the snarky animated figure couldn’t even respond to “Hello”. (You lost me at hello)

Still, just for fun, I’ve been meaning to implement yet another front end to [Eliza](http://en.wikipedia.org/wiki/ELIZA), but then I read about the more modern [AliceBot](http://alicebot.blogspot.com/) in Bruce Wilcox’s gamasutra article [Beyond AIML: Chatbots 102.](http://www.gamasutra.com/view/feature/3761/beyond_aiml_chatbots_102.php)

So I decided to have them talk to each other, using web-based  
[Eliza](http://www-ai.ijs.si/eliza-cgi-bin/eliza_script) and [AliceBot](http://alicebot.blogspot.com/) implementations. The conversation bogs down quickly:

Human: How can I help you?  
ALICE: Just keep talking to me as long as you can.  
Human: Do you wish to as long as me?  
ALICE: OK, I will as long as you.  
Human: Do you wish to will as long as me?  
ALICE: OK, I will will as long as you.  
Human: Do you wish to will will as long as me?  
ALICE: OK, I will will will as long as you.

