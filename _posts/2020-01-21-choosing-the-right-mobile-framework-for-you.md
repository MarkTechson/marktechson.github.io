---
layout: post
title:  "Choosing the right mobile framework for your project or business #30DaysofThreads"
date:   2020-01-21 13:30:00 -0500
categories: ['mobile', '#30DaysofThreads']
comments: true
post_id: 2866fdc8-acfc-4611-b35b-d3e09d75f9c8
summary: >
         You want to create a mobile app but aren't sure what's the right path, let's look at some options and see which makes the most sense for you.

---

# Choosing the right mobile framework for your project or business. [&#35;30DaysofThreads](https://learnwithari.com/30days/)

_Context: I am a Sr. Software Engineer (10+ years experience) with actual apps deployed on Google Play and the App Store._

First of all, you have to ask yourself this main question: Do I actually "NEED" a mobile app to accomplish my goals for my project. For example, if you have a blog or an online store, I would say you don't need an app. Yes, the idea feels really good to say you have an app BUT the idea of actually having something working and producing results is more important. Your pursuit of building a mobile app could radically slow down your progress and cost you a lot of money. It comes down to it being a business decision where you need to balance the factors. So, if you don't need a mobile app you can get a lot done by having a mobile responsive (websites that change the layout based on the size of the screen). A lot of website builders come with responsive design built-in. That's a win and you can keep going. If you need an example, think about how Amazon looks different on your laptop vs on your phone. Your site might be great just working like that.

If you have some custom functionality that goes beyond a store, for example, I would then look at "no-code" solutions. Check to see if there's something out 
that can help you to build your app with a little more customization. A quick [Bing search might help here.](https://www.bing.com/search?q=no+code+mobile+app+development&PC=U531&cvid=75a7a07b261f42e5a8e39bf9431daf2a&FORM=ANNTA1)

I don't have a recommendation here. But you can do a little research but here are SOME of the things to consider:

* Does it do what you need? 
* Does it fit your budget? How far can you go with it? Can it connect to my data?

You can technically ask this question across the board with any solution. Sometimes it just makes sense to do something as a stop-gap and then go from there. (This is from a startup perspective) 
If you are choosing for your established organization, then you'd have to ask even deeper questions about how this fits in your tech stack (which tools and technologies that you use at your company).

If you get to this point and you are deciding that you STILL want to build... 
Then I go into my next question: What skills do you have? If you know how to code or have someone on your team who can code you need to figure out what skills you have. Let's focus on a FEW core technologies. This is not an exhaustive list but can point you in the right direction 
If you know HTML/CSS/JS (Web):

I would say look into something like Ionic. They are probably the proven leader in the HYBRID Mobile App Space (meaning, you can install the app but it will use web tech to display your content/do the logic).

The app Sworkit used Ionic. 
Some of the benefits of using a HYBRID app are:

1. Speed of development
2. Potential Code re-use
3. CROSS-PLATFORM (this is probably the biggest win as you can create the app for iOS/Android) at the same time.

There are some cons, though. 
1. Performance MAY become an issue. This is not guaranteed and there have been some excellent advancements in this area but be aware. FB switched to Hybrid about 5 years ago and it went poorly.

2. Missing "Native Feel". You ever use an app and it just didn't feel like a regular 
app? Well, that could have been poor design or it could have been a hybrid app. Animations don't always work smoothly on a handset in hybrid apps. (This may NOT happen with your app)

3. Advanced features (like Face Unlock) may not be available for your tools yet. 
Do you know JavaScript really well?

There are a few really great tools that are industry-standard right now that can leverage your JavaScript skills and help you build Native Apps. These apps feel like apps that are made with the original tools (which we'll get to!) 
Two that are probably going to be the most vetted and highly recommended are ReactNative and NativeScript. Their names sound similar but they are very different in practice. If you already know React, then ReactNative is almost a given for you. You can take those React skills and get to work really quickly. If you know Angular or Vue (both are JavaScript frameworks) you might love Native Script. You'll get your app coded pretty quickly and these are really well documented, too! That means you'll find help when you do Google searches. Nothing is perfect!

It is possible to have apps that just don't fit with the limitations of this approach! For example, React Native has had a lot of challenges with the "right" way to navigate (move around) the apps. Airbnb recently announced that they are moving away from ReactNative. That doesn't mean you should, though! "Will it work for you" is the core question. Some of the downsides here are that these frameworks (like others I'll mention next) take time to get access to some phone features. These types of cross-platform (create 1x for both iOS & Android) are almost like using your friend's house. You have access to the parts of the house that have been cleared between you. But if something new is in the house, you have to have that conversation about whether or not you can use it. They might be slow to respond and you have to wait for access. But for this (minor) trouble, you get so much! You can build a polished app in no time.

Before we get to the core development option, there is one more category I'd like to bring up as something for you to consider: Non-JS Cross-Platform Apps. These apps don't use JavaScript but they allow for some of the best performance and feature richness in the space.

* Xamarin (uses a language called C#)
* Flutter (users a language called Dart)

These two (and I'm sure there are others, like RubyMotion) offer great performance and 
great developer experience. Full disclosure, my apps are written in Flutter even though I've tried out nearly all of the solutions I've mentioned. The architecture of these tools make it very easy to create high performance, fully-featured apps but require you to learn a new language. A huge benefit of the JavaScript-based (and even web-based) solutions is that getting those skills is more straight forward because of the boom in coding boot camps and online courses etc. These tools don't allow for skill-reuse if you don't already know the languages. 

Finally, if you know Java or Swift, then you are able to create whatever you want. But you lose the ability to write once and deploy to both platforms which may not be an issue if you have BOTH types of dev skills available to you. That's if you care about both iOS AND Android. What should you do? Choose the solution that gets your product out there. As long as you are "thinking" & in analysis paralysis, you are missing opportunities. Getting something out there so you can learn from it is top priority in most cases.

Good luck and thanks for reading! 