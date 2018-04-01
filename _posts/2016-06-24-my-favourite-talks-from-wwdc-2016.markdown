---
title: "My favourite talks from WWDC 2016"
layout: post
date: 2016-06-24 18:47
headerImage: false
tag:
- conferences
- WWDC
- ios development
category: blog
author: aleksanderpopko
description: Be sure to wear some flowers in your hair...
---
*Be sure to wear some flowers in your hair...*  
  
### Intro
WWDC is over. There is always the same problem with the San Francisco conference – so many interesting things, so little time to watch. Finally, I managed to find some spare time between everyday work and boxing trainings to spend a few hours in front of my Mac. Here are my favourite talks and some thoughts on the Keynote & Platforms State of the Union.


### [Keynote](https://developer.apple.com/videos/play/wwdc2016/101/) && [Platforms State of the Union](https://developer.apple.com/videos/play/wwdc2016/102/)
This year WWDC was, in my opinion, relatively tranquil. It was based on improvements of already existing solutions rather than showing to the world new and “amazing” stuff. If you were expecting fireworks, you could be a little disappointed, but hey, is focusing on great solutions to make them even better really that bad? I don’t find [neomania](https://aleksanderpopko.tech/fragility-neomania-ios-whats-developer/) – a love of novelty for its own sake, rational. Apple already revolutionized a lot of areas – personal computers, music, and smartphones – and this company became a main player on the market. Improving already existing solutions to be even more user friendly, rather than releasing new, innovative products that can result in a complete revolution or complete fiasco, seems to be a normal and rational step in company evolution.

Personally, I really appreciate things like:

* [Swift 3.0](https://swift.org/blog/swift-3-0-preview-1-released/)
* [Swift playgrounds for iPad](https://developer.apple.com/swift/playgrounds/)
* speed enhancements in watchOS 3
* changes in iMessages
* new kits in iOS 10 SDK

### [Going Server-Side with Swift Open Source](https://developer.apple.com/videos/play/wwdc2016/415/)
Although server-side applications are not my piece of cake, I am really impressed with the possibilities of using Swift on different platforms other than iOS, watchOS or macOS. Using Swift for developing client and server applications at the same time sounds like a dream. The demonstration of [Kitura](https://github.com/IBM-Swift/Kitura) – IBM web framework and HTTP server for Swift and [IBM Cloud Tools For Swift](http://cloudtools.bluemix.net/) was really impressive and its potential results in high hopes and serious expectations for the future.

### [Protocol and Value Oriented Programming in UIKit Apps](https://developer.apple.com/videos/play/wwdc2016/419/)
Do you remember [Protocol-Oriented Programming in Swift](https://developer.apple.com/videos/play/wwdc2015/408/) and [Building Better Apps with Value Types in Swift](https://developer.apple.com/videos/play/wwdc2015/414/) from WWDC 2015? For me these talks were game changers. Before watching them, I treated Swift like “Objective-c with nicer syntax”. Then my eyes opened. In Protocol and Value Oriented Programming in UIKit Apps, Jacob and Alex continue this approach and, by using value types and protocols for developing view layers of simple apps, show that immutable values are not limited to simple model types. I really believe in this approach- immutability, local reasoning, relying on protocols rather than on superclasses, using enums for mutually exclusive states, composability instead of inheritance. All these things are great and result in cleaner, more reusable and less error-prone code.

### [Improving Existing Apps with Modern Best Practices](https://developer.apple.com/videos/play/wwdc2016/213/)
A lot of information from this talk is widely known, so no new, revolutionary things here – just some basic, yet valuable, insight on how to improve code quality and modernize apps with little effort, which is always a good thing.  

### [Understanding Swift Performance](https://developer.apple.com/videos/play/wwdc2016/416/)
This advanced talk touches low level stuff – memory plus performance, and shows how structs, classes, protocols, and generics are implemented in Swift. It’s great for those who like to know how their code works underneath, how to optimize code for performance, and how to choose the right abstraction mechanism.
