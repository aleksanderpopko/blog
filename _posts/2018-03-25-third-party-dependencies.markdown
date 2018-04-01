---
title: "Against third party dependencies"
layout: post
date: 2018-03-25 15:44
headerImage: false
tag:
- software development
- philosophy
category: blog
author: aleksanderpopko
description: Rational way of using third party dependencies.
---
*It's not the daily increase but daily decrease. Hack away at the unessential.*  
Bruce Lee, [Tao of Jeet Kune Do](https://www.goodreads.com/book/show/57858.Tao_of_Jeet_Kune_Do)  

### Intro
Consider the following scenario: a bunch of developers are working on short-term project from scratch. The client is in a rush, so they decide not to reinvent the wheel and use as many external dependencies as humanly possible. Pace of development is ridiculous. After a few weeks there are many closed tickets in [Jira](https://www.atlassian.com/software/jira). Nice. Everybody is happy.  

After a few months, there are very many third-party dependencies and very little code the developers can fully control.  

And after a few years there is a project that's horribly hard to maintain. Some of dependencies are no longer supported. The language version has changed and the client needs to pay for forks maintenance. Oh, and in the meantime, there was a little security issue in one of those seventeen external frameworks...  

### Three questions

Third party open source libraries are great. They are (usually) polished up to the limits of what's possible. Using them is (usually) a pleasure. They were (usually) developed by people much smarter than I, whose work I highly admire. ***Chapeau bas* for developers who spend their own time on making life easier for other developers.** However, using them always brings in some risk - and that could be a problem.


* What happens if the library is no longer supported? Are you ready for bearing the costs of maintaining the fork? Or maybe a migration to another solution and huge refactoring will be cheaper?
  
* What happens if there is a security flaw? It's not an unrealistic scenario - it's enough to recall [the case of the popular AFNetworking](https://gist.github.com/AlamofireSoftwareFoundation/f784f18f949b95ab733a). Adding third party code always brings in the risk of [increasing potential undetected vulnerabilities](https://hackernoon.com/im-harvesting-credit-card-numbers-and-passwords-from-your-site-here-s-how-9a8cb347c5b5).

* What happens if your requirements change after a few months? Your project is changing and the third-party frameworks are changing. At some point, the overlapping paths might diverge significantly. You may need features that the already integrated third party does not offer or ones provided for in an unacceptable way. What will you do then?

### Summary

**I'm not against using third party libraries, I'm against losing control of the code and taking unnecessary risks.** Before adding another third-party dependency to your project, consider if it is really necessary. Think what can happen if it stops being supported. What the cost of migration to another solution or fork maintenance could be. Don't get me wrong - third party code is not the root of all evil. It is useful, it helps to deliver things faster and to increase overall productivity. It's all about balancing the risk with the pay-off. If you decide to use a third-party dependency, protect yourself with appropriate design and a reasonable layer of abstraction.

Be like the [ancient stoics](https://dailystoic.com/what-is-stoicism-a-definition-3-stoic-exercises-to-get-you-started/) - always keep the worst possible scenario in mind.
