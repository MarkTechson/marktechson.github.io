---
layout: post
title:  "Getting Started with ReactJS"
date:   2016-03-19 13:30:00 -0500
categories: reactjs install
---
Getting started with React can be seriously daunting. One thing I have trouble with is the WHY must I do something. I've broken down some of the initial steps and concepts that I think you'll need to know to get yourself started with React. This won't be a tutorial as I think there are a bunch of resources out there. I want to give you enough to be dangerous and overcome the hump with getting up and running.

# Knowing What You Need to Install
The first thing you come across when looking at a React tutorial is the list of things you have to install. Looks something like:

{% highlight bash %}
npm install html-webpack-plugin webpack webpack-dev-server babel-{core,loader} babel-preset-react —save-dev
{% endhighlight %}

This list alone seems to be pretty intense if you are coming from a JQuery background or Angular background (which is where I'm from). Immediately I freaked out because most tutorials just started by saying "Install these to get started." But again - WHY?! **Here's why:** React has combination of language features and tools working in concert to deliver the promises made by framework. Broken down, each of these tools makes sense if you know what you need them for.

# First Up: Babel

What the heck is Babel you ask (I know I did)? It's a transpiler that will allows the brave among us to write code that is future compliant (e.g., ES2015, ES2016 and BEYOND!). This is a great proposition since one of the hardest parts about being a Front End Developer is knowing having to read about all the new features you can't use until all of your clients move from IE9. Babel makes that process less painful. In React, Babel is used for ES2015+ features AND the JSX language used to define UI components.

{% highlight bash %}
npm install babel-{core,loader} --save-dev
npm install babel-preset-react --save-dev
{% endhighlight %}

_I don't always write React code, but when I do I use JSX_

# Next: WebPack

If I were giving awards, I'd award the webpack team for having a great tool that noone knows exactly how it works and what it does! Webpack is a multi-tool that will do things like run your babel transpilation, start up a web server for development (or you can use the python SimpleHTTPServer like the rest of us!) and many more features. All of this is due to it's processing of loaders (modules that can extend the functionality of the tool.) In React-land, it's used to run Babel, help create your dist HTML file and bundle your code. These are incredibly helpful because they start to take the drama out of dependency management (though you still need to deal with npm for new packages). Now these don't look so scary, right?

{% highlight bash %}
npm install html-webpack-plugin --save-dev
npm install webpack --save-dev
npm install webpack-dev-server --save-dev
{% endhighlight %}

If we put it together, we get our bootstrap command of:

{% highlight bash %}
npm install html-webpack-plugin webpack webpack-dev-server babel-{core,loader} babel-preset-react —save-dev
{% endhighlight %}

# And Let's not forget why we came: React!

React is split into two primary modules: ```react``` and ```react-dom```. In short - the core logic for react is separated from the DOM specific functionality since react is also used for ReactNative.

Here's what the commands for these two look like:

{% highlight bash %}
npm install react react-dom
{% endhighlight %}

# The Finish Line At LAST!

With the two commands run in your terminal you'll be ready to get started with what seems to be a great framework. But wait, won't you need to know _what_ to do now?

Thanks for playing, stay awesome.
