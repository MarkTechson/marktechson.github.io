---
layout: post
title:  "Why I left NativeScript"
date:   2016-07-26 01:22:00 -0500
categories: ['JavaScript', 'NativeScript']
comments: true
post_id: e6fb5aa4-c576-4f06-8b47-c1c819360829
summary: >
         My honest experience wit NativeScript with a couple months of using it.
---
I write this blog post from my desk at 1:03AM frustrated admittedly but clear on my direction moving forward. First off, I want to be clear that I do believe that there is value in NativeScript as a framework, but I think that as a production tool, it is not ready. There is one caveat, if you are not using Angular2 support in NativeScript the experience could be entirely different.

Without too much ceremony, the primary reason I decided to move away from NativeScript was due to the fact that I kept fighting with the framework. More than once I spent hours trying to use an angular feature that wasn't working as advertised in NativeScript. The straw that broke the camel's back was around trying to make an HTTP request. Here's an example:

{% highlight JavaScript %}
    this._loginService.login(this.user).subscribe(
        (data) => alert(data),
        (err) => alert(err)
    );
{% endhighlight%}

This code snippet is supposed to use a service I wrote that connects via HTTP to a simple node server REST api and subscribe to the observable stream. Upon trying to run this code, I'd get a crash from the app and a message saying that __something__ wasn't implemented. What wasn't implemented? I can't be sure the because the stacktrace is misleading. After doing some research I noticed that this issue had been around in other places, too and had been reported to the Telerik team behind the Angular2/NativeScript integration but the solution felt like too much of a hack. And there within lies my issue with the framework as a whole - everything is so new and there are so many moving parts. The setup requires one to use Angular2 (new), TypeScript (new to many), NativeScript (new to many) and a concert of core modules from both Angular2 and NativeScript. Whne one of these gets out of sync (i.e., a new version is released) there is a big to-do in order to get your environment up and running again.

I simply couldn't bring myself to spend another 4 hours just trying to make the system play nicely. I'm moving on. Hello, ReactNative, what have you to say?

Thanks for playing, stay awesome.