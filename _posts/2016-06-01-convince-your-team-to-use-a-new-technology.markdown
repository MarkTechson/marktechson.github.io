---
layout: post
title:  "Convince Your Team to use a new Technology"
date:   2016-06-01 13:30:00 -0500
categories: ['JavaScript', 'es6']
comments: true
post_id: d3f4498d-c2c3-49c0-b479-0fb381684398
summary: >
         It can be tough to get your team to commit to new technology. Here are some thoughts on how to accomplish that.
---
I mentioned in a [previous post]({% post_url 2016-05-06-favorite-es6-feature %}) I said that you should really be using ES6 features right now. I say that because there are features that increase developer productivity on top of addressing some shortcomings of the language. I'm sure you're on board with the idea but have some issues convincing decision makers to make the necessary steps to make this happen. In this post I'm going to walk you through some three guidelines that can help you to accomplish that goal.

# TLDR;
Know the ___Why___, ___How___, ___When___ of this change before even presenting the idea.

# WHY
Your personal excitement for this new framework/library/IDE/etc is understandable and can be compelling to some of your peers, however, this isn't enough to get it integrated. There have been so many times in which I've wanted to introduce a new technology to my team. I came in bright eyed and excited but folded under the weight of a simple question: WHY?

As much as I wanted to say, "because this is _What the rest of the industry_ is doing now" - that answer, while potentially valid, doesn't hold as much weight as one would expect. Your organization is unique and a generic answer is nearly never the case. Thus, the first step in this process should be to figure out why you want to bring in this this new thing. The why can be difficult to word at first because _you_ know why this tool is great but you can't seem to get the buy-in that you are looking for. Take a step back and try to speak to the particular problem this solves and why it solves it to the best of your knowledge. The best of your knowledge implies that you have spent the time researching existing solutions and competitive technology. In this step, be okay with someone bringing up a point that you don't know the answer to. It isn't your job to be subjective here - do yourself a favor and be as objective. I like to ask myself the tough questions before even suggesting a new thing. I try to tear it down myself to be sure that I know my facts. Word of caution: __LEAVE YOUR PERSONAL VIEWS OUT OF THIS DISCUSSION__.

If we take the example of getting ES6 in our codebase the why could be something like:
* New features increase developer productivity and reduce chances for errors. For example (these help!), fat arrow functions allow us to keep the binding of the outer _this_ context which can be a confusing area for developers. This binding will help us to reduce the risk of misunderstanding introducing bugs.
* Going to a newer version makes our upgrade path easier later. Teams using JDK6 well past the end-of-life now have a large task ahead of them to migrate to JDK8, we can avoid a similar situation by migrating now. (using a comparative example helps to bring people into the idea)

# HOW
This step can come out of nowhere. It's very easy to spend all of our time trying to prepare to defend the why of our suggestion to only neglect the step where we outline the game plan for how we'll integrate it into our team. Again, the simple "just do it" isn't applicable here. This is where you'll have to start to put yourself in the shoes of not only your team lead/manager but also in those of the other team members. Integration of new tech can cause a disruption in the flow of everyday work. Continuing with our ES6 example, the manager may ask some of the following questions:

* What about older browsers?
* What happens if the industry moves away from the tech?
* How do we make this a seamless transition for the team?

Not being prepared for these types of questions will sink your idea __quickly__. These questions may seem to be specific to JavaScript, but try to think of them more generally. Instead of reading _what about older browsers_ read instead: _what about legacy support_ or even more generally __how does this fit into the way we're currently doing things?__ To answer this you need to do your homework and have some solutions already in place. For ES6, I would recommend adding something like __Babel__ to the toolchain and removing it when the browsers have more standard support for the newer web standards. This answer eleminates the use of some transpilers, but that's okay - compromise is a major key here. Take note of the bigger point - it is important to do due diligence in this situation. In regards to the other questions, adding the support for ES6 using Babel means that team members can just start working in ES6 now or ES5 (as they currently are). Also, if the transpiler is added to the build tool chain and removed in the future there is no difference (aside from extra logging) to the team. Your solutions may not wrap up into a pretty bow like this but at least be as prepared as possible to increase your chances of success.

# WHEN
Finally, the when can be just as important as the why and how. Timing is everything. No matter how cool a technology is, introducing it before a release is probably not going to be the right time. Of course, there are exceptions to this rule but the general idea is the same: choose a time that makes sense for your team. There are changes that have required me to put a pin in it until 6 months later where we can circle back to it. If you don't have the patience to wait that long, then you aren't ready for introducing new things. Teams move at different speeds and recongnizing that is critical for your own success. If the timing is wrong it can break down your __how__. One of the things that managers look for is maintaining developer productivity and that is jeopardized when a new component is added to the stack. There are outside influences to consider as well. Your new technology may be lower on the totem pole than business needs. Companies are designed to be profitable first and then a great haven for developers second. When trying to figure out how to answer this question start thinking realistically about the state of the team. Are there any deployments on the horizon? Do we need this new tech now or can it wait (what's the urgency)? Once you can objectively identify a good time for the change then you have all the puzzle pieces in place and now it's time to make it all happen.

# Final Words
Every developer will need to make a case to get new technology introduced to a team. It is critical for your chances of success to spend some time researching the __WHY, HOW and WHEN__ for your suggestion. This isn't a 100% science, though. Even answering all of these questions can lead to rejection. In that case I would say that it is better to try to find a compromise. Once the compromise is found rinse and repeat. Eventually you'll get where you want to be.

Thanks for playing, stay awesome.