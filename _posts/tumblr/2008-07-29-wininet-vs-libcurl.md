---
layout: post
title: wininet vs. libcurl
date: '2008-07-29T23:26:31-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110242908556/wininet-vs-libcurl
---
When I worked on an Internet gateway for a startup named Neomar at the end of the dot-com boom, I made the mistake of writing an [HTTP](http://www.w3.org/Protocols/) implementation from scratch. It’s a good way to learn the nitty-gritty of HTTP, but in retrospect, it would have made sense to use some an already-mature HTTP library. Recently, I had some more HTTP work come my way, and this time I looked at [Wininet](http://msdn.microsoft.com/en-us/library/aa383630(VS.85).aspx), which comes native with Windows, and [libcurl](http://curl.haxx.se/libcurl/), a popular cross-platform library. Wininet of course has the advantage of being already there, but it has the painful inelegance typical of Microsoft API’s (at least up til .NET) Take this example from the [Microsoft Knowledge base](http://support.microsoft.com/kb/q165298/) of how to create a POST request:

    static TCHAR hdrs[] = \_T("Content-Type: application/x-www-form-urlencoded"); static TCHAR frmdata[] = \_T("name=John+Doe&userid=hithere&other=P%26Q"); static LPSTR accept[2]={"\*/\*", NULL};

    // for clarity, error-checking has been removed HINTERNET hSession = InternetOpen("MyAgent",INTERNET\_OPEN\_TYPE\_PRECONFIG, NULL, NULL, 0); HINTERNET hConnect = InternetConnect(hSession, \_T("ServerNameHere"),INTERNET\_DEFAULT\_HTTP\_PORT, NULL, NULL, INTERNET\_SERVICE\_HTTP, 0, 1); HINTERNET hRequest = HttpOpenRequest(hConnect, "POST",\_T("FormActionHere"), NULL, NULL, accept, 0, 1); HttpSendRequest(hRequest, hdrs, strlen(hdrs), frmdata, strlen(frmdata)); // close any valid internet-handles

Compare with a POST example from the [libcurl tutorial](http://curl.haxx.se/libcurl/c/libcurl-tutorial.html):

    curl\_easy\_setopt(easyhandle, CURLOPT\_POSTFIELDS, data) curl\_easy\_setopt(easyhandle, CURLOPT\_URL, "http://posthere.com/"); char \*data="name=daniel&project=curl"; curl\_easy\_perform(easyhandle); /\* post away! \*/

The libcurl example is missing a couple of function calls to be complete - one to initialize libcurl, and one to clean it up. On the other hand, the wininet example is missing a few cleanup calls (one for each of the three HINTERNET handles created), and, a bigger pain, it doesn’t take a URL - you would have to call InternetCrackURL and allocate a structure that receives the URL components, then use those components in the example calls. I’ve just started on this project, but I’m ready to declare winner.
