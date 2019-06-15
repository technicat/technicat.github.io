---
layout: post
title: WorkedOn.Com
date: '2012-05-13T13:30:20-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515859446/workedoncom
---
On my deathbed, I might regret watching too much TV, but more likely I’ll rue all the hours I’ve wasted on my resume. Years ago, I wanted both a PDF and HTML version of my resume so I spent some time trying to create an XML definition from which I could generate those formats by applying XSL stylesheets, and then because recruiters always want Word format, I ended up dabbling in the JFOR open source project so I could get RTF output. I also had some vision of some mobile compatibility so you could walk around with a Palm device (that lets you know when I was thinking about this) at a job fair and sync resumes with a recruiter. I still think that’s a cool idea, that I just didn’t execute on, and maybe it’s doable or done already for iOS (if you want to run with this idea, please send me stock options, or a promo code).

I also have a vision of some kind of deluxe web resume, more like a portfolio really, in which you can embed rich content (photos, videos, even Flash and Unity webplayers), way more interesting than the bland LinkedIn portfolios, and maybe some kind of social networking (yeah, bandwagon, bandwagon…) - but not “friend me” stuff, but more project-centered, so you can see who worked on the same project or at the same company. And personally, I think it would be fascinating to visualize the flow of people from and through projects and companies. I even had a domain I will use for this super site - [workedon.com](http://workedon.com/).

But for now, I’ve wimped out and placed my PDF resume generated from my LinkedIn profile on workedon.com. It does solve one current problem, where recruiters contact me on LinkedIn, say they love my resume and can they have a copy of my resume, I say hit the PDF button, they say I can’t find it, can you add me to your network, or can you give it to me in Word? The site does technically have a PHP script, redirecting you to the PDF (it’s a step up from my previous use of the HTML meta refresh tag, which I now realize from wikipedia is considered “legacy”):  
`
<?php`

header( ‘Location: [http://workedon.com/PhilipChu.pdf’](http://workedon.com/PhilipChu.pdf') ) ;

?\>

