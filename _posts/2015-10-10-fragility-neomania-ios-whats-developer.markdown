---
title: "Fragility, neomania, and iOS: what’s in it for you, Developer?"
layout: post
date: 2015-10-10 11:02
headerImage: false
tag:
- philosophy
category: blog
author: aleksanderpopko
description: Cognitive biases. Financial derivatives. Old is good. How to code in unpredictable projects we don't understand?.
---
*Cognitive biases. Financial derivatives. Old is good. How to code in unpredictable projects we don't understand?*

>Now close your eyes and try to imagine your future surroundings in, say, five, ten, or twenty-five years. Odds are your imagination will produce new things in it, things we call innovation, improvements, killer technologies, and other inelegant and hackneyed words from the business jargon. These common concepts concerning innovation, we will see, are not just offensive aesthetically, but they are nonsense both empirically and philosophically. 

**Nassim Nicholas Taleb.**

### From finance to philosophy

The first time I encountered Nassim Taleb’s works was a few years ago, when I was studying finance – something that, on the surface, may seem starkly different from philosophy or software development. Taleb focused on options theory (Dynamic Hedging: Managing Vanilla and Exotic Options). What is an option? It’s a financial instrument with an asymmetrical payoff based on the value of other assets. Pricing an option involves mathematical models, probability theory along with some trading strategies and heuristics.

After quitting his job as an options trader, Taleb embarked on a journey of philosophy with an attempt to transfer his views on probability onto other areas, not only finance. His main concept is this: the most important areas of human life – society, state, economy, science, politics, wars, health – are influenced by randomness and highly unpredictable events, called [Black Swans](https://en.wikipedia.org/wiki/Black_swan_theory). A Black Swan is an unforeseeable, outlying event with great scale and extreme effects. Examples of Black Swans? The discovery of penicillin, the rise of the Internet, World War II, the collapse of the USSR, the subprime mortgage crisis or terrorists attacks. Taleb’s works ([Fooled by Randomness](https://www.amazon.com/gp/product/0812975219?ie=UTF8&tag=aleksanderpop-20&camp=1789&linkCode=xm2&creativeASIN=0812975219), [Black Swan](https://www.amazon.com/gp/product/081297381X?ie=UTF8&tag=aleksanderpop-20&camp=1789&linkCode=xm2&creativeASIN=081297381X), [Antifragile](https://www.amazon.com/gp/product/0812979680?ie=UTF8&tag=aleksanderpop-20&camp=1789&linkCode=xm2&creativeASIN=0812979680)) convey a comprehensive philosophy about how to successfully handle an unpredictable environment.

Taleb groups things into three categories: fragile and highly prone to Black Swans, robust – not influenced by Black Swans at all and, finally, antifragile – things that benefit from chaos, volatility and disorder. The aim is to eliminate the fragile from our lives.

**But how to determine what is fragile and what is not?**

One factor is time – if something has been used for a long time, it has probably experienced a lot of volatility and has been well tested over a long trial period. So, generally speaking, older solutions that are still in use tend to be less fragile than the latest inventions.

According to Taleb, one phenomenon that makes people prone to Black Swans is “neomania” – a love of novelty for its own sake. **Neomania revolves around the rejection of old, tried and tested solutions for fresh ones, just for the simple reason that they are new.**

> Consider the futuristic projections made throughout the past century and a half, as expressed in literary novels such as those by Jules Verne, H. G. Wells, or George Orwell, or in now forgotten narratives of the future produced by scientists or futurists. […] Our world looks too close to theirs, much closer to theirs than they ever imagined or wanted to imagine. And we tend to be blind to that fact—there seems to be no correcting mechanism that can make us aware of the point as we go along forecasting a highly technocratic future. […] Those people who engage in producing these accounts of the future will tend to have (incurable and untreatable) neomania, the love of the modern for its own sake.

**Taleb, Antifragile**

### How do fragility, neomania and software go together?
I’m generally fond of sharing Taleb’s concepts, but hey, how does that all fit in with how I make a living? I work as an iOS developer and I’m writing this blog post during my break between coding mobile apps. To my right, there is an iPhone lying on the desk with the silent mode switched on so as not to distract me from the task in hand. What is more, I am typing this text on a Macbook, and there is a strong likelihood that you are reading it on some kind of electronic device. Make no mistake – technology does matter.

**Is it possible to relate Taleb’s ideas to software development?** For a long time, I used to think that this is a totally different world, with different rules, and the fact that I pay my rent by developing mobile apps tended to block out Taleb’s concepts in this area. A turnaround came a few months ago, after I heard [Ash Furrows’](https://ashfurrow.com/) talk about the value of new and old technologies.

### Neomania in iOS development
<iframe width="560" height="310" src="https://www.youtube.com/embed/FZHBk1XMvEA" frameborder="0" allowfullscreen></iframe>
Ash Furrow – Evolution of Asynchronous Programming on iOS

Although Ash didn’t use the word “neomania” or make any reference to Taleb’s philosophy, he did raise an important issue – **iOS developers tend to swap old technologies for new ones without really considering the context.** He went through the history of iOS asynchronous programming and described the advantages and disadvantages of particular solutions – explaining that what is crucial in choosing a solution is not its age, but its context of usage.

Ash brilliantly pointed out why this kind of neomania is so popular among iOS developers, but I think a lot of these aspects can apply to developers in general.

One of the reasons is a kind of cognitive bias. **Humans are always looking for patterns.** They make our life simpler so that we don’t need to analyze every situation and every possibility, just apply a pattern and it – hey presto – it usually works. However, this might not necessarily lead to the best result.

When you start learning iOS, you follow the most popular practices. You were probably really bad at these practices at first – because you were really bad at programming on the whole (it’s worth coming clean here that a lot of iOS developers, including myself, had no programming background before switching to develop on iOS, so they started with no knowledge at all about design patterns, best practices, etc). Your mind was drawn to a simple conclusion – you extrapolate your incompetence onto the solution itself. In other words, **you convinced yourself that this old, popular solution was wrong.**

When a new concurrent solution comes out, by this time the chances are that you will have made some serious improvements to your iOS skill set compared with the first steps of your adventure. **Your mind naturally makes the inference – a new solution is better.**
This is the line of thinking I followed when I started learning about blocks. I was fascinated by this solution and I used (or rather – overused) blocks everywhere I could. I became so obsessed with this idea to the point where I couldn’t even imagine starting a new project without installing [BlocksKit](https://github.com/BlocksKit/BlocksKit). Pure neomania.

There are some other reasons why we prefer the latest solutions – iOS is constantly changing. **With every WWDC there are new features, new APIs, new solutions, simply put – new things to learn.** There is no better way to learn than to practice coding, so we naturally prefer new solutions when we can.

Finally, Apple is really good at marketing. This refers not only to new devices, but also to new solutions from the developer’s perspective.

### Decisions based on context
Ash suggested we choose solutions depending on the context, rather than their age. Try asking yourself some contextual questions:

* What technology is available?
* How much do myself and my team understand the available options?
* How steep is the learning curve?
* How much time do I have to complete the task?
* How stable are the tools available?

**Different solutions work for different problems, and old solutions still have benefits.** According to Ash, ”old” is stable, well documented, easy to hire for (i.e. it’s easier to find an Objective-C developer than a Swift developer) and has a lot of helpful resources, libraries and tutorials.

### Summary
The goal of this blog post wasn’t to discuss topics like Objective-C versus Swift, storyboard versus xibs, NSOperation versus GCD, or any other individual preferences. Like in the world described by Taleb, the context of developers’ decisions is always to some extent unknown and unpredictable (i.e given the codebase or the clients’ decisions about new features).

When working in IT, a little bit of neomania might creep in subconsciously to your decision-making processes. For different reasons, we may have a tendency to choose new, glossy solutions instead of the old favourites. There’s nothing wrong with that, but it’s worth remembering that the oldies might have some extrinsic benefits you might not notice at first glance.

Originally posted on [netguru blog](https://www.netguru.co/blog/fragility-and-neomania-ios-developer).
<br>
<br>
<br>
<br>
*This site contains affiliate links. If you decide to buy a book on Amazon by going through one of them, I will receive a commission. You can find more information [here](https://affiliate-program.amazon.com/).*
