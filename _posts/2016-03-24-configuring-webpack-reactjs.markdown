---
layout: post
title:  "Unpacking WebPack and ReactJS"
date:   2016-03-24 13:30:00 -0500
categories: reactjs install
summary: >
         WebPack is a critical part of the ReactJS toolchain, in this post we'll explore configuration.
---
In [my previous post]({% post_url 2016-03-19-getting-start-with-reactjs %}) I started by breaking down the different components that need to be installed to get started with using the framework. There's a critical component that is notoriously _under-documented_ and that is [WebPack](https://webpack.github.io/). Before we can configure it, we need to understand a little more about it.

# Why WebPack
Think of WebPack as a bit of a magic door - code files go in with and new version of those files come out. Based on the configuration (which we'll cover here) a different version of those files comes out as a bundle (of joy?). These transformations allow us to work in one medium and then have our code converted into a neat bundle that we can include in our HTML. For example, when writing code using modules (pre-ES2015) the code will look like:

{% highlight JavaScript %}
var fooModule = require('foo-module');

// Use our foo module
fooModule.doSomethingCool();
{% endhighlight %}

The modular pattern we are using here is great for working, however the code won't work in browsers as is. We are in a similar situation with using SASS. The code needs to be transformed to be used. Enter WebPack. I'm sure there are multiple ways to accomplish these transformations (Grunt or Gulp Plugins...or Brunch) but the recommendation seems to be WebPack by the team at Facebook. Enough warm-up, let's get _packing_.

# Configuration Step One: Understanding the Parts
When an app (React app, in this case) is bundled with WebPack we'll want the code included somewhere. WebPack has a plugin that will help us do just that. It's called ```html-webpack-plugin```. This allows us to replace a part of our html code with some generated code. In the React world, this is going to be used to tie in our bundled app (JS) code into our html.

Taking a look at the ```webpack.config.js``` :

{% highlight JavaScript %}
var HtmlWebpackPlugin = require('html-webpack-plugin');
var HtmlWebpackPluginConfig = new HtmlWebpackPlugin({
    template: __dirname + '/app/index.html',
    filename: 'index.html',
    inject: 'body'
});
{% endhighlight %}

In the above section we have two things going on:

- First we are importing the module we need
- We create a new object and pass it some configuration information

The first item we've seen a bunch of time, the second one is more interesting to me. In brief - we specify the file to do the processing on and then we tell the plugin what the output name should be and which component to replace with our bundled content.

The ```template``` attribute specifies the source content for our HTML. Think of it as a standard file where we'll have our includes for css (if they are not being packed by WebPack). Here is an example template:

{% highlight HTML %}
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Hello, World</title>
        <link rel="stylesheet" href="/path/to/stylesheet.css">
    </head>
    <body>
        <div id="app"></div>
    </body>
</html>
{% endhighlight %}

The ```filename``` attribute specifies the name of the output file. This will be put in the ````dist``` directory for the output of the process.

Finally, the ```inject``` property tells where to place the ```<script>``` tag for including our output file.

With this object being configured, we'll hold on to it because we still haven't told WebPack what to do with it. More configuration information can be found [here](https://github.com/ampedandwired/html-webpack-plugin).

# Configuration Step Two: Putting it together
We've configured the html-webpack-plugin, now it is time to configure the export for the module variable. There are four properties we'll configure:

```entry``` - the file that we'll supply to be transformed

```output``` - where to put the results of the transformations

* ```path``` - the location to place the file(s)
* ```filename``` - the name of the bundle file that'll be created

```module``` - this is where things get interesting. The loaders - which are just a set plugins that we'll use to apply to the to our entry file. One of modules we'll want to use in our React app is a loader called [Babel](https://babeljs.io/). In short - React uses JSX for some easier html-esque code for components. The loaders property is an array, so we can have multiple loaders with multiple configurations. Our babel loader looks like this:

{% highlight JavaScript %}
{
    ...    
    module: {
        loaders: [
            {test: /\.js$/, exclude: /node_modules/, loader: 'babel-loader'}
        ]
    }
}
{% endhighlight %}

Though this may seem like a what the heck moment, let's break it down to make it more digestible. It breaks down to the following:

* test: a regex to figure out which files to apply our loader operations to
* exclude: which files to not apply the transforms to
* loader: the name of the loader we want to use

We can always add more loaders in the future, but for what most people are doing this is a good place to start.

```plugins``` is a also an array. As mentioned before, a WebPack configuration can have multiple parts to it. Remember our object we created for the ```html-webpack-plugin```? Here's where we'll use it:
{% highlight JavaScript %}
{
    ...
    plugins: [HtmlWebpackPluginConfig]
}
{% endhighlight %}

Wow! That was a lot of stuff going on there but when it is broken down into segments it all becomes easier to read. Let's have a full look at the configuration:

{% highlight JavaScript %}
var HtmlWebpackPlugin = require('html-webpack-plugin');
var HtmlWebpackPluginConfig = new HtmlWebpackPlugin({
    template: __dirname + '/app/index.html',
    filename: 'index.html',
    inject: 'body'
});

module.exports = {
    entry: [
        './app/index.js'
    ],
    output: {
        path: __dirname + '/dist',
        filename: 'index_bundle.js'
    },
    module: {
        loaders: [
            {test: /\.js$/, exclude: /node_modules/, loader: 'babel-loader'}
        ]
    },
    plugins: [HtmlWebpackPluginConfig]
};
{% endhighlight %}

# Final Step: Configure Babel for React
We need to create a configuration file so that the babel loader actually knows what type of thing to do. Considering that - in ```.babelrc``` we need the following content:

{% highlight JavaScript %}
{
    "presets": [
        "react"
    ]
}
{% endhighlight %}

# DONE
As I mentioned from the start - WebPack can be a bit confusing to get started with. Hopefully in the future the documentation will be improved to make getting started much easier. Until then, you can bookmark this page or look for a pre-seed kit to get you started.

Good job on sticking around to the end - more content on the way.

Thanks for playing and stay awesome.
