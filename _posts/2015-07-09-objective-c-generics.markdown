---
title: "Objective-C generics"
layout: post
date: 2015-07-09 22:18
headerImage: false
tag:
- ios development
- objective-c
- technical
category: blog
author: aleksanderpopko
description: Finally something new in Objective-C.
---
*Finally something new in Objective-C.*  
  
### Intro
Sure, last WWDC was all about Swift. That’s a given. After progressing to 2.0, becoming open source, and introducing protocol extensions and a [new error handling API](https://netguru.co/blog/error-handling-swift), Apple’s young child has grown into a heavy-hitter and deservedly captured the audience’s attention. But in the world of iOS development, good old Objective-C is still in the game, and WWDC 2015 brought a notable new feature. Without further ado, Ladies and Gentlemen, let me talk a little about Objective-C Generics.

### Objective-C generics
Take a look at this code:

{% gist aleksanderpopko/803ddba56d2208f2e1e700bf21a4f213 %}

Nothing complicated, we have a class, `Person`, with three properties. Although it should be a struct, for the purpose of this blog post (a comparison with Objective-C) we decided to use class. We have the property `friends` – an array that holds `Person` objects. Swift’s `Array` type is a generic collection. It can hold any type that is created in Swift. Now, assume that we have an object of class `Person`, and we need its first friend name.

{% gist aleksanderpopko/f00d69bd86204ed755c522f0f6c94678 %}

Compiler knows that `person.friends` is an an optional array that holds `Person` objects, so `firstFriendName` type is optional String. Great.

How will it look in Objective-c?

{% gist aleksanderpopko/2a4ae415d95c6ca198699a4349251f1b %}

Before we go further, let me talk a little about nonnull and nullable property attributes. These are called nullability annotations and were introduced with Xcode 6.3. A `__nullablepointer` can have `nil` or `NULL` value, while a `_nonnull` one cannot. If you break these rules, the compiler will let you know.

Now, we can go back to generics. We couldn’t define the type of elements in our `friends` array. As in the Swift example, assume that we have an object of class `Person`, and we need its first friend’s name. Due to the lack of generics, we first need a variable assigned to the first element of the array:

{% gist aleksanderpopko/e689f570b17d8faf0b7b4997c8208b80 %}

Because of no generics in Objective-C, `person.friends.firstObject` is of type `id`, not `Person`. `id` is a pointer to any object, which means it can be any object created in Objective-C. We don’t know explicitly that `person.friends.firstObject` is an instance of `Person`. We can assign `person.friends.firstObject` to a variable of type `Person`, but also it could be any other type, for example `NSString`.

{% gist aleksanderpopko/a914a63e9924f8dcee3bab034133410f %}

The responsibility for using the right type lies with us. If we use a wrong type and, during runtime, a message that an object doesn’t respond is sent – then a runtime error will occur.

To get the first friend name, we need to create another variable:
{% gist aleksanderpopko/a783b6988c43e515ffb348ea9923ef40 %}

This example is really simple, but it shows that Objective-C demands additional code and it’s the developers, not the compiler, that will be responsible for an object’s type tracking.

If Objective-C were jealous of something from Swift, Java or C#, it would probably be generics (just google „objective-c generics”). Hopefully, Xcode 7 and Objective-C Lightweight Generics come to the rescue:
{% gist aleksanderpopko/9003f889dc02c0090f9905d705aea1c7 %}

Now we can define the type of values which are in a collection!
{% gist aleksanderpopko/6098fa7d87566108d7dd316ba837824e %}

The compiler knows that `firstFriendName` is type of NSString. What happens if we assign an object from a collection to a variable of incorrect type?
{% gist aleksanderpopko/7c8dbaa0c43acd52af49b3f694146932 %}

We get a compiler warning. Nice.
Look how Swift imports the Objective-C Person class:
{% gist aleksanderpopko/6a8773902532cb3d93a4987edd67381f %}
Lightweight Generics don’t apply only to `NSArray`. They can also be used with two other of Foundation’s collection classes – `NSDictionary` and `NSSet`.
{% gist aleksanderpopko/f86900c45f6f1a42dc99ca9dc17b8c48 %}

What’s more, you can use Objective-C Lightweight Generics in your custom classes:

{% gist aleksanderpopko/3fd80d07971d1e641a03c507cde537e4 %}

{% gist aleksanderpopko/13df0dee7526d3d0d5fc74202fbac391 %}

What happens if we use the wrong type?

{% gist aleksanderpopko/83f7bee33aaf6e1c85a74e4c0af85892 %}

The compiler will behave as before and give us a warning.

Bear in mind that now Objective-C generics in custom classes behave a little different than in `NSArray`, `NSSet` and `NSDictionary`. They are ignored by Swift. If we import them into Swift, they will be treated as if they were unparameterized. [Fortunately this will change with Swift 3](https://github.com/apple/swift-evolution/blob/master/proposals/0057-importing-objc-generics.md).

### Summary
What is the result of introducing Objective-C lightweight generics in Xcode 7? The necessity of typecasting is reduced. Responsibility for tracking an object type is moved from developer to compiler. The code is cleaner, type safer, and less prone to error. But that’s not all – before Xcode 7 you needed to be careful when working with Objective-C frameworks in Swift. Every object from an Objective-C collection needed to be cast as `AnyObject`. Introducing Objective-C generics resolves this problem and results in better Swift – Objective-C interoperability.

Originally posted on [netguru blog](https://www.netguru.co/blog/objective-c-generics).
