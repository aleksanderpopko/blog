---
title: "I’m new to iOS development. Should I start learning Swift or Objective-C?"
layout: post
date: 2016-11-17 20:02
headerImage: false
tag:
- ios development
- swift
- objective-c
category: blog
author: aleksanderpopko
description: TL;DR Start with Swift, if necessary learn Objective-C later.
---
*TL;DR Start with Swift, if necessary learn Objective-C later.*  
  
### Intro
These days we have some programming language dualism when it comes to iOS development. For years, iOS apps were created using Objective-C. In the middle of 2014, Apple announced Swift – new programming language, and within two years, this young cub, became heavy-hitter and a real game changer. Before we determine if it is better to start learning iOS development with Swift or Objective-C, lets review how it started, what was the reason behind Swift genesis, and what is the current status?

### Long long time ago…
Everything begins in the early ’70s, when [C language](https://en.wikipedia.org/wiki/C_(programming_language)) was developed and used to rewrite the [Unix operating system](https://en.wikipedia.org/wiki/Unix). What are C features? C is procedural (there is one main program, and many procedures that can be called and executed from the main program), imperative (you write a program like you are writing sentence in imperative mood – “do something… then do something else… then if something happens do something”) and low-level (it basically means that however program is fast and efficient, development process is time-consuming, error prone, unpleasant and developer needs to know a thing or two about hardware and memory). C became one of the most popular programming languages of all time, with compilers available for the majority of existing computer architectures and operating systems. C is still in use, for example, when it comes to programming microcontrollers. You can even sometimes find code written in this language in iOS projects, especially when it comes to low-level stuff, where memory matters.

In the ‘80s another programming language was developed – [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk). Contrary to C, Smalltalk was object oriented. What are objects? It’s a conception of a thing which may contain data (“attributes”, which means “how object looks”) and code (“methods”, which means “what object can do”). Objects are created when program runs and they can interact between themselves (please pardon this loose, intuitive definition).

### But hey, what does C and Smalltalk have in common with iOS development?
Two people – Brad Cox and Tom Love, inspired by Smalltalk features, started working at their company Stepstone on the implementation of an object-oriented extension to C. In 1988, a book titled “Object-Oriented Programming, An Evolutionary Approach” was published, which contains the description of Objective-C. In the same year, NeXT licensed Objective-C from StepStone. NeXT developed two important frameworks that have strong influence on current iOS development: AppKit and FoundationKit.

A few years later, in 1996, Apple acquired NeXT. This is how Objective-C landed in the company which manufactures iPhone in the future and that is the reason why Objective-C is so popular when it comes to iOS apps development.

As we can see, Objective-C is quite old. This is probably why Apple started working in 2010 on their new programming language – Swift. Four years later Swift was publicly released. Language was constantly evolving, and in 2015 it became open source. Evolution is not finished – Apple encourages people to share ideas how Swift can be improved. Proposals about Swift Evolution are collected and reviewed in [Swift Programming Language Evolution](https://github.com/apple/swift-evolution) public repository on Github.

### How does Swift differ from Objective-C?
First of all, it doesn’t hold C and Smalltalk heritage. Syntax is cleaner and has better readability. It supports type inference, which results in cleaner and less prone to error code. What’s more, Swift has all these nice features that modern programming language should have: generics, fast and concise iteration over collections, tuples, multiple return values, native error handling and functional programming patterns.

### So should I start learning Swift or Objective-C?
Objective-C has existed for years. A lot of projects are written in this language. There are thousands of tutorials, video tutorials, [GitHub](https://github.com/) repos, books and [Stack Overflow](http://stackoverflow.com/) questions and answers. If you look through job offers, this programming language is still demanded. So maybe starting learning Objective-C before Swift is good idea? I believe it’s not.

### Why learning Swift before Objective-C seems more rational?
* **Learning Swift gives a lot of fun.** I’ve got two, totally different reminiscences of my beginnings with new programming language. When I was learning Objective-C ranting, grumbling, complaining and desire to quit were on my daily agenda. On the other hand, when I was learning Swift there was fascination how simple things can be, a lot of “eureka moments”, and pure joy how intuitive this language is with comparison to Objective-C (ok, I have programming experience then, so learning process can be easier, but my experience was still TOTALLY different). This is not only my individual opinion – Swift got first place for Most Loved Programming Language in the [Stack Overflow Developer Survey 2015](http://stackoverflow.com/research/developer-survey-2015#tech-super) and second place [one year later](http://stackoverflow.com/research/developer-survey-2016#technology-most-loved-dreaded-and-wanted).

* **Learning process is faster.** As Swift syntax is easier and cleaner, you can focus on solving problems, using concepts and patterns or getting familiar with commonly used frameworks. It’s IMO more important than wondering where to put colon, semicolon, brackets, angle brackets, square brackets or spending time trying to understand a particular block of code because of highly unreadable syntax.

* **Good programming habits.** Swift encourages the use of good programming habits. Generics, protocols, functional stuff, optionals – all these things invites a developer to good, modern programming practices like using composition over inheritance, or writing rather declarative than imperative code.

* **All learning resources are already available.** There is ton of stuff that can be helpful with learning Swift: videos, blogs, courses, tutorials and books (but I don’t recommend books about Swift, as this language is constantly changing). Also on Stack Overflow there are many Swift related topics. There are a lot of great WWDC videos. What is more – Swift has great community (just take a look at [Swift Evolution](https://github.com/apple/swift-evolution)).

* **Apple is now focused on Swift.** Look at the [last WWDC](https://developer.apple.com/videos/wwdc2016/) and see how many videos about Swift there are. Some Sierra and iOS 10 stuff are currently using significant amount of code written in this language: new Music app, Sierra Console app, Mission Control, Documentation Viewer on Xcode etc. If Apple emphasize Swift also we should.

* **Swift is ready for commercial projects.** New versions of Swift led to regular complains by developers who use it in their projects. It’s nothing unusual – migrating code, dealing with frameworks that don’t support newest version of language, potential errors – all of these things can give you a headache. However, Swift is now successfully used in some commercial projects. For example, [LinkedIn rewrites their two apps to Swift](https://realm.io/news/kamilah-taylor-kyle-sherman-swift-at-linkedin/). There are also iOS developer job offers where Swift is preferred language (although the number is smaller when compared to Objective-C).

* **Swift can spread outside Apple’s ecosystem.** Apple adopted Objective-C from NeXT, and no one else did this, so this language is in reality not used outside Apple’s world. As Swift is open source, things can be different. Even now there are frameworks which give utility beyond iOS and OSX development- for example, [Kitura](https://github.com/IBM-Swift/Kitura) or [Perfect](http://perfect.org/).

### So… is Objective-C useless?
No. There are still many companies that hold and maintain projects with thousands lines of Objective-C code. There are still many great frameworks, written in this language. It is well known, tested over years and still popular. And there are many iOS developer job offers that requires it. Objective-C is still in the game, but it’s definitely harder and more unpleasant to learn.

### Summing up
When you start learning iOS development, the most important things are concepts, patterns and knowledge of popular frameworks. In my opinion, programming language is secondary. There are two main reasons why Swift is better to putting first steps in iOS development:

* learning process is faster and more pleasant
* we can assume that Swift will become industry standard in the future

I believe that the rational strategy is to start with Swift, get familiar with Xcode, frameworks, design patterns and all iOS stuff, and later, if there will be a necessity, learn Objective-C. And I really envy people who have possibility to start learning programming with Swift, instead of ugly, old child of C and Smalltalk.
