---
layout: post
title: Checking for ARMv6
date: '2012-04-09T14:19:00-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515845161/checking-for-armv6
---
I stopped supporting ARMv6 devices a while ago (I’m still building fat binaries with ARMv6 support on iOS, but that’s just because the App Store submission process won’t let me drop previous ARMv6 support - practically speaking, the recent iOS’s don’t run on those devices anyway). However, during some Unity code cleanup I found the function that I used on iOS and Android to perform a runtime check to see if I was running on ARMv6 and thus needed to deactivate some content to run with decent performance. I’m tossing that code out, but here it is, if you ever need it:

`
static function IsARM6() {
return (SystemInfo.processorType.IndexOf("ARMv6")>-1);
}`

