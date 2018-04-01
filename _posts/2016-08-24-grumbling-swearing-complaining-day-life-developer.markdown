---
title: "Grumbling, swearing and complaining – a day in the life of a developer"
layout: post
date: 2016-08-24 23:45
headerImage: false
tag:
- philosophy
category: blog
author: aleksanderpopko
description: How to rant, grumble and complain in friendly way?
--- 
*How to rant, grumble and complain in friendly way?*

### Proloque
***Senior Dev:** Now you just gotta learn how developers talk. You just listen to the way Martin and I banter back and forth. You OK? You’re ready?<br>
**Junior Dev:** Sir!<br>
**Senior Dev:** Alright let’s go in…*


### Intro
I swear a lot. Especially during the development process. Xcode crashes, long-as-hell compiling time, dealing with spaghetti code, overuse of singletons, my own stupid mistakes, overnight changes in mockups, [technical debt](https://en.wikipedia.org/wiki/Technical_debt), unannounced changes in backend, and design anti-patterns in legacy code – all of these occur more or less often during a developer’s work. Add to this mixture my typical Polish melancholic-querulous nature and several years spent on mats with wrestlers and boxers who are not necessarily ultra-cultural guys and you will have a perfect candidate for grumbling-vulgar-developer-who-is-liked-by-nobody. How to stay professional, remain friendly to your colleagues and at the same time not allowing your hidden emotions to destroy your mental health? Here are some concepts that (I hope) really help me in everyday work:

### Criticise bad solutions in general, not people who use them
Just think about these two statements:

>This class that John wrote now has 1300 lines of shitty spaghetti code and this singleton is keeping all the state of an application. Good luck with testing.

versus:

>I really don’t like singleton-based application architecture. The shared mutable state can cause problems with the unpredictable behaviour of the app. We should think about refactoring some classes, what about trying a dependency-injection approach? As a result we should have a more testable project.

I think the difference here is obvious, isn’t it?

### Remind yourself of the times you wrote some horrible code
No one is perfect. Nothing is as good an ego killer as the reminiscence of some of your own code that you’re ashamed of. It’s even better if the code is at least still in use and someone is complaining about it 😉

### If you really feel the necessity to complain, complain about common problems
Things like Xcode crash, a slow Mac, or bad internet connection are quite common occurrences. Complaining about these things is much better, than complaining about someone’s code. Everyone has had similar problems, at least once, so it will be much easier to find a common language, and no one will be seriously insulted.

### Focus on your code quality
If you really like to show how “code should look”, direct your anger to writing the best code you can. With perfect, consistent style, nice documentation, proper usage of the design patterns and short, standalone classes. This is much better and advantageous than complaining and insulting someone else’s work.

### Start using devRant instead of bothering your team members
[devRant](https://www.devrant.io/) is a community of developers who like to… complain. You can anonymously (or not – as you wish) complain about a project, legacy code, IDE, programming language limitations or whatever. Moreover, there is a possibility to upvote and downvote other complaints and discuss them. I love this place – in contrast to twitter or [stackoverflow](http://stackoverflow.com/), we don’t have to act more likeable than we really are.
### Never ever let emotions to get into a code review process or interactions with a client
I was taught, that code review is for improving software, not for insulting other developers or trying to prove that one code is better than another. Being as no-offensive as possible, and trying not to take code review too personally will help you keep an objective approach. When reviewing someone’s code, be concrete, precise, and if you think something can be done better – propose your own solution, do not only select the “fix this” option. Code review is not only a way to monitor code quality, but also a great tool for learning – I really like to read the discussions related to pull requests, even in projects that I don’t contribute to.

A similar issue involves interactions with clients. Client’s goals are probably different to yours. Usually a developer does not see the whole picture. Spending two months on rewriting an app from the scratch is not necessarily a good idea – however beautiful and elegant the code will be, this probably will have zero business value. Remember, that your perspective in the project can be really vast, and someone else can have a very different point of view.

### Summing up
This probably wasn’t a politically correct blogpost about zen-like, egoless programming. I agree – being humble and friendly to environment and emotionless when it comes to dealing with extremely shitty legacy code is an archetype of the perfect developer. But sometimes things really suck and you have to deal with it. If you really need to rant or complain, do this right way.
### Epilogue
***Martin, the Swift Dev:** Perfect! An imperative-programming-guy and a Junior!<br>
**Senior Dev:** How ya doing Martin, you wannabe Haskell dev?<br>
**Martin, the Swift Dev:** Senior! You cheap bastard! I should have known you’d come in, I was having such a pleasant day!<br>
**Senior Dev:** What’d you do? Rejected some pull requests? Or code some highly functional stuff, that nobody understands, even you?<br>
**Martin, the Swift Dev:** Who’s this guy?<br>
**Senior Dev:** Ohh… He’s a new iOS dev in our company. I’m trying to show him what our job looks like… You see Junior, now that’s how devs talk to one another. Now you go out and come back in and talk to him like a dev, like a dev in our company.<br>
**Junior Dev:** What’s up ya wannabe functional Haskell dev? Have you code highly functional stuff, that nobody understands, even you?<br>
**Martin, the Swift Dev:** [taking the keyboard and pointing at Junior Dev] Get out of my project before I reject all your pull requests! Go!<br>
**Senior Dev:** Take it easy, take it easy!<br>
**Senior Dev:** [to Junior Dev] What the hell are you doing? Have you lost your mind?<br>
**Junior Dev:** But that’s what you said. That’s what you said developers say.<br>
**Senior Dev:** You don’t just come in and insult the developer in his own project! You just don’t do that. What happens if you meet a stranger? You get the wrong one, and none of your pull requests will be accepted!<br>
**Junior Dev:** What should I have said then?<br>
**Martin, the Swift Dev:** Well… why don’t you start with… eeehm… Hi or Hello…<br>
**Senior Dev:** Yeah, just come in and say… eeeehm… I’d like to code something in this project if there are any tasks in backlog.<br>
**Martin, the Swift Dev:** Yeah, be polite, but don’t kiss ass.<br>
**Senior Dev:** In fact you could even talk about a long compiling time, complain about Xcode crashes or not enough RAM in your Mac.<br>
**Martin, the Swift Dev:** eeeehm… Damn, I just spent 15 minutes on compiling and eeehmm Xcode build the project but the derived data wasn’t removed and I need to build the project again!<br>
**Senior Dev:** Yeah, if you need to complain, don’t swear on codebase or other dev’s work, just talk about obvious things.*

Inspired by [Gran Torino](https://www.youtube.com/watch?v=LHYa3XbBPIM).
