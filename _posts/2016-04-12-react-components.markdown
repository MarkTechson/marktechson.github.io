---
layout: post
title:  "Components in React"
date:   2016-04-12 13:30:00 -0500
categories: ['reactjs']
comments: true
post_id: d64141b7-2833-4210-bb8d-90296ef26a2e
summary: >
         In React/ReactNative Components and component design can mean success or failure in your project.
---
One of the crowning achievements in React (from my humble opinion) is the focus on components. A valuable part of these components is the ability to create declarative UI definitions and domain specific languages (DSL). In order to achieve maximum success with any framework it is important as a developer to exploit the strengths of the framework. Therefore, take advantage of components in React.

React allows for modular design with its component classes. As with any design pattern it is important not to over design your components but to break them down into logical chunks with single responsibility and composition as a design goal.

Let's break down a weather widget.

# Design Gist
Our widget will have three components: the temperature in degrees fahrenheit, an image representing our current conditions and a description of the same conditions. Considering this design, my mind automatically goes toward breaking down the components into three pieces:

* Image component used to display the image
* Degree component used to display the degree
* Description component use to display the description of the current condition

This may seem like overkill depending on which framework you are using (ReactJS vs React Native) but there's a method to the madness. If we are thinking of creating a DSL, then describing out layout semantically gives us a nice abstraction (non-leaky, more on this later).

Consider the following:

{% highlight JavaScript %}
function WeatherWidget(props) {
    return (
        <div>
            <degree val={props.degrees}></degree>
            <image src={props.imageSrc}></image>
            <description text={props.description}></description>
        </div>
    );
}
{% endhighlight %}

# Why the extra work?
In our example above, it could have been easily written without the extra components but the value here is that anyone looking at this can tell what each component is used for. The better thing? That the components don't tell the user anything about their formatting (nor does she need to know anything about it!). This is what I mean when I talk about a leaky-abstraction. These occur when an api requires implementation details to be available just to use it. For example, if you needed to know how the ```degree``` component worked just to use the component, then there's an issue. Of course, with all software, there are exceptions to the rule. If an api is has strange behavior looking at the source code can be valuable.

# My two cents
Here are a few guidelines I keep in mind when making components:

* Create single responsibility, composable React components.
* Keep them as stateless as possible! If you have some data to display, then send in the data
* Consider making your components into a domain specific language (DSL) so that you can create semantic UIs

If I follow these rules, I end up creating things that are reusable and better designed.

Stay Awesome.
