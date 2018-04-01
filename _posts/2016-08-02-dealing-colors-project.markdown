---
title: "Dealing with colours in the iOS project"
layout: post
date: 2016-08-02 20:25
headerImage: false
tag:
- ios development
- technical
category: blog
author: aleksanderpopko
description: When it comes to UIColor, usefulness is in simplicity.
---
*Usefulness is in simplicity.*  
  
### The problem

Just imagine, you got beautiful app mockups from the designer, with perfectly specified colours in RGB or hex format (or you only got colourful mockups and had to ask “Hey, what’s hex for this button?”). Surely some colours will occur many times in different mockups for the same app. Also, during the app development process, the UX team may change the app appearance many times. How we can define constant values of colours in an elegant, clean, and easy to change way?

**Hardcoding colours’ values in views or view controllers is really a bad idea** – maintaining the code, or changing it when mockups are updated can be unpleasant. What about using preprocessor macros? This is also far from perfect, as more debugging friendly solutions are available.

### Swift 
The approach that I particularly like is the widely known use of extensions for UIColor**:

{% gist aleksanderpopko/4a24750d4d60a02761a26c7cf63f47ff %}
### Objective-C
In Objective-C we use the UIColor category. Just remember about prefixing to [avoid category methods names clashes](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/CustomizingExistingClasses/CustomizingExistingClasses.html):

{% gist aleksanderpopko/d7a08c9ab54546aa607d77af252b31df %}

{% gist aleksanderpopko/f33e10d66a4fc2e3f598ddb42d75c241 %}

Take a look at differences between documentation in Objective-C and Swift files. If you still have doubts, read these two great blog posts:

* [Documentation by Mattt Thompson](http://nshipster.com/documentation/)
* [Swift Documentation by Mattt Thompson and Nate Cook](http://nshipster.com/swift-documentation/)

### That's all, Folks!
That’s all you need. This approach results in a clean and convenient way of using colour values in the project. Of course, this idea is not limited to UIColor – e.g. extensions or categories can be successfully used when dealing with other aspects, such as fonts.
