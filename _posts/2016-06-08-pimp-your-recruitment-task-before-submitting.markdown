---
title: "Pimp your recruitment task before submitting"
layout: post
date: 2016-06-08 16:43
headerImage: false
tag:
- ios development
- recruitment
category: blog
author: aleksanderpopko
description: Grinding and polishing. Everything is important, and especially nil. Coding with style.
---
*Grinding and polishing. Everything is important, and especially nil. Coding with style.*

### Introduction
So, you’re facing the typical scenario – saw interesting iOS developer position, sent a resume and were assigned a coding task. It doesn’t matter if you are being asked to create custom control, something with networking and parsing JSONs or a simple app with maps. It doesn’t matter if it is simple or difficult – a few things can always be done to add a finishing touch. Here are some tips, based on my experience on both sides of the recruiting process.

### Be sure that all task requirements are met
This refers to both scope and instructions. Sending a partially complete task is really a bad idea. It is better to send an email saying that task will be sent in one day later, rather than handing in an incomplete task. What is more – be sure that you’re following instructions. If using storyboards is forbidden – use xibs or build your views programmatically. If Objective-C is demanded, use Objective-C, not Swift. It can look trivial and obvious, but such situations occur quite often.

### Add a [readme](https://en.wikipedia.org/wiki/README) if the project is not ready to build
Does the project use [Cocoapods](https://cocoapods.org/), [Carthage](https://github.com/Carthage/Carthage) or [Git Submodules](https://git-scm.com/docs/git-submodule)? Or does it demand some pre-build configuration? If your work falls into this category, instructions on how to run the project should be added. The developers reviewing recruitment tasks are usually doing so in their spare time between their everyday work. Giving them an extra work load just to investigate and make assumptions on how to run your project is probably not the best idea.

### Use a consistent style guide
Compare these two pieces of code:
{% gist aleksanderpopko/d0e332eb10efdd11c597d9915018ab3d %}
and
{% gist aleksanderpopko/f6c8d95dd33e54f4e24d5c15e9b6c15c %}

Although, the only differences are a matter of style, the second one definitely makes a better impression. Use a single, consistent style for your project. Here are two examples that I really like:

* [The Official raywenderlich.com Swift Style Guide](https://github.com/raywenderlich/swift-style-guide)
* [The Official raywenderlich.com Objective-C Style Guide](https://github.com/raywenderlich/objective-c-style-guide)

### Use third party libraries rationally
When you have a few views in the app and are using autolayout, installing [Masonry](https://github.com/SnapKit/Masonry), [PureLayout](https://github.com/PureLayout/PureLayout) or other similar stuff can be helpful. Installing [Alamofire](https://github.com/Alamofire/Alamofire) or [AFNetworking](https://github.com/AFNetworking/AFNetworking) to perform one or two requests within the whole project is really pointless.

### Use Objective-C generics and nullability annotations
These features are relatively new in Objective-C. Take a look:
{% gist aleksanderpopko/4ea29b08a4acfa2c3c4857485ca91813 %}
and
{% gist aleksanderpopko/858a76192900f2daaaaa31b6376aa3ff %}
The second approach results in a code that is cleaner, safer, and less prone to error. It demands very little effort, but leads to higher code quality. For those who are not familiar with these features, take a look at these two blogposts:
* [Objective-C Generics](https://aleksanderpopko.tech/objective-c-generics/)
* [Nullability and Objective-C](https://developer.apple.com/swift/blog/?id=25)

### Use NSLocalizedString for strings visible by user
This is another indicator of code quality and elegance. Even if working on a simple recruitment project that will not be internationalized, using [NSLocalizedString](https://developer.apple.com/documentation/foundation/nslocalizedstring) is a good idea – it shows awareness, thoughtfulness, and an eye towards the future.

### Write unit tests
Unit tests are crucial. I suggest writing them during the development process, but if they are absent, adding them will be really beneficial. The recruitment task probably doesn’t require a lot of logic – so implementing unit tests shouldn’t be too time consuming. I highly encourage writing tests in [BDD](https://www.objc.io/issues/15-testing/behavior-driven-development/) style, using [Specta](https://github.com/specta/specta) & [Expecta](https://github.com/specta/expecta) (Objective-C) or [Quick](https://github.com/Quick/Quick) & [Nimble](https://github.com/Quick/Nimble) (Swift). These frameworks allow the creation of highly readable unit tests, which is really helpful for the reviewer.

### Write documentation
Documenting public methods is useful for developers – when I come back to code after a few months, the documentation reminds me what’s going on. Moreover – writing documentation results in cleaner and more elegant code. If creating documentation is problematic, this probably means that there is something wrong with the code e.g. the method is wrongly named. Documentation is beneficial to the developer, but it is especially important for other users of his code. Remember, during recruitment process you are not writing code for yourself, but for a reviewer, who probably will not have a lot of time to dig deeply to understand it.

Here are two great blogposts about writing documentation:

* [Documentation by Mattt Thompson](http://nshipster.com/documentation/)
* [Swift Documentation by Mattt Thompson and Nate Cook](http://nshipster.com/swift-documentation/)

### Summing up
Implementing these simple tips makes code cleaner, more readable, and improves its overall quality – all at a low expense of time. I encourage to use these suggestions not only for recruitment tasks, where code needs to be read and assessed in a short period of time, but also to incorporate these habits in everyday work. Spending a little additional time on small improvements that have huge impact on code quality is always a good idea.
