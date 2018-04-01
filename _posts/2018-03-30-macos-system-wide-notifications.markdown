---
title: "macOS: system-wide notifications"
layout: post
date: 2018-03-30 16:18
headerImage: false
tag:
- macos development
- software development
- objective-c
- technical
category: blog
author: aleksanderpopko
description: Pretty straightforward yet pretty useful interprocess communication utility.
---
*A straightforward yet pretty useful inter-process communication utility.*

### What are system-wide notifications? 

Apple’s documentation says:

>These routines allow processes to exchange stateless notification events. Processes post notifications to a single system-wide notification server, which then distributes notifications to client processes that have registered to receive those notifications, including processes run by other users.

In short, they give us the possibility to communicate between different processes. [Brett Terpstra wrote a nice tutorial](http://brettterpstra.com/2012/07/04/quick-tip-system-wide-notifications-with-notifyutil/) about how to use system-wide notifications with Terminal. How can we use them in Objective-C programs?

### Let's code!

Let’s start with creating new Objective-C command line tool in Xcode.
<br />
![1]({{ "/assets/images/notifications1.png" | absolute_url }})
<br />
![2]({{ "/assets/images/notifications2.png" | absolute_url }})
<br />
Next, we need to import `notify.h` into the `main.m` file.

{% highlight raw %}
#import "notify.h"
{% endhighlight %}

And finally, post notification.

{% gist aleksanderpopko/d5e94df4f6f2e19a0ffe1731f8bec9fd %}

`notify.h` is written in C, and that’s perfect because Objective-C is a superset of C.

To receive notification in a different process we need to register monitoring for this notification. Let's open Terminal and type:

{% highlight raw %}
notifyutil -1 com.aleksanderpopko.notify.first-notification && echo "notification received"
{% endhighlight %}

`-1` means we are waiting for only one notification. After running our Objective-C command line program, we should receive the notification in Terminal.

{% highlight raw %}
notification received
{% endhighlight %}

Pretty cool. Now, let's register a new notification using Objective-C.    

{% gist aleksanderpopko/acbc1681df49c3bb376dd3ced4e83073 %}

I believe the code is self-explanatory. We are using `[[NSRunLoop currentRunLoop] run]` to keep our program running. When a notification is received, the Xcode console will log our `notification received` information. To post the notification from Terminal just type:

{% highlight raw %}
notifyutil -p com.aleksanderpopko.notify.second-notification
{% endhighlight %}

That’s all for now folks. Thanks for reading!