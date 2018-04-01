---
title: "Scripting in Swift: short introduction"
layout: post
date: 2018-02-19 16:15
headerImage: false
tag:
- swift
- technical
- software development
category: blog
author: aleksanderpopko
description: Swift as a scripting language.
---
*Surströmming, salmiakki and automation.*

### Intro

Two months ago, I've heard that there is a possibility to write and execute scripts in Swift. Damn, why it is so niching? Why I wasn't aware and I struggled with everything in bash? 

### Compiled Languages vs Scripting Languages

Before we start, let's recall the basics. There is recognized dichotomy of programming languages. Compiled languages require compiler, which translates our source code into binary. Then binary is run on the machine. This is what we used to do when it comes to developing iOS and macOS apps.

Scripting languages give a possibility to run a source code directly in some other application (called [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing))). As there is no compiling step, we don't need compiler. In this case, development is usually faster and simpler, but performance is much lower. Scripting languages are very often use for automation and avoiding repetitive tasks.  
  
That's needed to say: compilation versus scripting is not determined by language per se. It is a matter of adopted tools and solutions. There are languages that can be both scripting and compiled, and Swift is one of them.  

### Prerequisites

So, what do you need to start scripting in Swift? The list is fortunately not so long:

* macOS. I only used Swift on Apple's operating system. There is a possibility to run [Swift on Linux](http://blog.krzyzanowskim.com/2016/03/23/status-of-portable-swift-code/), but, I've never played with that so I couldn't tell anything more.
* [Command Line Developer Tools](https://www.macissues.com/2014/05/26/what-are-the-command-line-developer-tools-in-os-x/). If not installed, it will be automatically downloaded when needed. Don't bother about this.
* Text editor. Just a matter of preference - you need a tool to write your scripts. I prefer [Sublime](https://www.sublimetext.com/), but it is really up to you.
* [Xcode](https://developer.apple.com/xcode/) (optional). This tool is really powerful, and for simple scripts, it can be too heavyweight. However, code completion, \`jump to definition\` option and access to Foundation's documentation could be useful.

### REPL

[REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop), which is an acronym of read-eval-print-loop is a simple, interactive development environment. It gives a possibility to write single code expression, execute it, and immediately print the result. Let's take a look.

Open Terminal app and type \`swift\`.
{% highlight raw %}
Welcome to Apple Swift version 4.0.3 (swiftlang-900.0.74.1 clang-900.0.39.2). Type :help for assistance.
1>
{% endhighlight %}

Now you can type Swift expressions - REPL will execute them and print output.
{% highlight raw %}
1> print("Hello World")
Hello World
2>
{% endhighlight %}

You can declare variables, constants, and even use functions.
{% highlight raw %}
1> let x = 2
x: Int = 2
2> func duplicate(number: Int) -> (Int) {
3.     return number*2
4. }
5> duplicate(number: x)
$R0: Int = 4
6>
{% endhighlight %}

If you need to leave REPL just write \`:q\` and press enter.

To learn more about Swift REPL, I recommend [official blog post](https://developer.apple.com/swift/blog/?id=18).

### HelloWorld.swift

Now we will leave REPL and move to writing very simple Swift script. First, we need to create Swift file:
{% highlight raw %}
$ touch HelloWorld.swift
{% endhighlight %}

Now, we can open HelloWorld.swift file and add some Swift code.
{% highlight raw %}
print("Hello World")
{% endhighlight %}

To execute our first script, just type \`swift HelloWorld\` in Terminal.
{% highlight raw %}
$ swift HelloWorld.swift
Hello World
{% endhighlight %}

We can also make files executeble. Before setting as executable, we need to remember about putting [shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)) in our HelloWorld.swift file.
{% highlight raw %}
#!/usr/bin/swift
print("Hello World")
{% endhighlight %}
This small line of code in top of the file is responsible for running script using proper interpreter. We can make file executeable using [chmod](https://en.wikipedia.org/wiki/Chmod) +x or swiftc:
{% highlight raw %}
$ swiftc HelloWorld.swift
$ ./HelloWorld
Hello World
{% endhighlight %}

### Selenops

Writing \`hello world\` using new tools is always exciting as hell, but let's take into account something more serious. [Selenops](https://github.com/zntfdr/Selenops) is a very simple web crawler, developed by [Federico Zanetello](https://twitter.com/zntfdr).   

I think the code is self-explanatory, but there are three really important aspects:

* taking  command line arguments
* [URLSession](https://developer.apple.com/documentation/foundation/urlsession) usage  
* doing something usefull

With scripting in Swift we can enjoy all the benefits of powerful [Foundation](https://developer.apple.com/documentation/foundation) (and even external dependencies), but what it is more important, we can develop stuff that can solve real problems.  

### To be continued...

Scripting in Swift is great. iOS developers are usually not very fluent in anything else than Swift or Objective-C. I can write some shell scripts, but on my scale of pleasure, it is somewhere between eating Swedish [surströmming](https://en.wikipedia.org/wiki/Surstr%C3%B6mming) and Finnish [salmiakki](https://en.wikipedia.org/wiki/Salty_liquorice). Swift gives us the power of automation using our well-known tools in our well-known world. We are no longer doomed to use Shell scripts, Python or Ruby. This is so fascinating, that you can expect next posts on this topic very soon.
