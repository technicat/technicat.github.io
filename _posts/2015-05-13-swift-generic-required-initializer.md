---
layout: post
title: Swift Generic Required Initializer
date: '2015-05-13T00:28:10-07:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/118840178186/swift-generic-required-initializer
---
More Swift madness. Without the required initializer, the generic built with that type generates bad\_access crashes.

class WEObject {  
 &nbsp; &nbsp;var ID:Int=0

&nbsp;&nbsp; required init() {}

}

class Dict\<T:WEObject\> {

&nbsp; &nbsp;var dict = [Int:T]()

&nbsp; &nbsp;func Find(ID:Int)-\>T {  
 &nbsp; &nbsp; &nbsp; &nbsp;if (dict[ID] == nil) {  
 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;let route = T ()  
 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;route.ID = ID  
 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;dict[ID] = route  
 &nbsp; &nbsp; &nbsp; &nbsp;}  
 &nbsp; &nbsp; &nbsp; &nbsp;return dict[ID]!  
 &nbsp; &nbsp;}  
}

