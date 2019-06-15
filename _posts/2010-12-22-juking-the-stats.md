---
layout: post
title: Juking the Stats
date: '2010-12-22T04:20:50-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110411995351/juking-the-stats
---
A recurring theme in the series The Wire is “juking the stats”, the practice of juggling numbers (crime figures, test scores…) to assuage politicians and the public. I’ve noticed this practice lately with bug databases. Actually, the most egregious violation I’ve witnessed was on a console game project several years ago, where the publisher instructed us on the gold master date to mark all the bugs in the database as closed. It’s one thing to stop working on the project, it’s quite another to present the grand fiction, “the product shipped, therefore it’s bug-free."&nbsp; More recently, I’ve noticed the less egregious but perhaps more insidious practice among some vendors of auto-closing bug reports under some circumstances, e.g. if there has been no recent activity.

The various reasons may seem debatable, but it seems to me there is an underlying wrong assumption - that closing a bug report is a good thing. Sure, fixing a bug is a good thing, but the state of a bug database should represent the "truth” of the product. In fact, you want to see the open bug count increase during much of the project - that indicates the product is progressing and getting tested and the engineers know what to work on. And even toward the end of a project, think of the open bug count as your reality stick with which you can bludgeon management. One company president kept insisting on new features even in the last few weeks before the scheduled ship date, until I pointed out there were still 300 open bugs in the database listed as “major” (that’s another thing, don’t mess with the priority of bugs - major bugs don’t turn into minor bugs and minor bugs don’t become major. The bug DB is not a micromagement tool). When in doubt, leave the bug open. If there’s not much going on with it, mark it as a “cold case”. Imagine how each episode of Cold Case would turn out if the cases were treated like bugs - “This man was murdered twenty five years ago. Whodunit? Who cares. Case closed.”

