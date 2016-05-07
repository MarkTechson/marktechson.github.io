---
layout: post
title:  "My Favorite JavaScript ES6 Feature"
date:   2016-05-06 13:30:00 -0500
categories: ['JavaScript', 'es6']
comments: true
post_id: c3941111-ea5b-4467-8f19-550e878b348c
summary: >
         ES6 has a many cool features and this one is my favorite.
---
If you aren't using ES6 (ES2015) you really should be. There are a lot of new features that are going to up your productivity and make writing code a little less confusing. Of all the many features to use my favorite at this moment is Template Strings!

Remember doing the following:

{% highlight JavaScript %}
var first = 'Mark';
var last = 'Techson';
var age = 'Over 9,000';

var greeting = 'Hello, my name is ' + first +  ' ' + last + ' and my age is ' + age + '!';

console.log(greeting);
{% endhighlight %}

In my contrived example, I'm using three variables and putting them together to get the greeting is definitely doable but I find that this is cumbersome. I always have seem to make a mistake with matching up my quotes or my plus signs.

With Template Strings we can use back-ticks (i.e., ``` ` ```) and simplify our greeting code.

{% highlight JavaScript %}
var first = 'Mark';
var last = 'Techson';
var age = 'Over 9,000';

var greeting = `Hello, my name is ${first} ${last} and my age is ${age}!`;

console.log(greeting);
{% endhighlight %}

Using the ```${}``` pattern with our variables we get string interpolation and a cleaner, much easier to read string. We can also do some fun things around multi-line strings, too. The following is legal:

{% highlight JavaScript %}
var first = 'Mark';
var last = 'Techson';
var age = 'Over 9,000';

var greeting = `
    <div>
        Hello, my name is ${first} ${last} and my age is ${age}!
    </div>
`;

console.log(greeting);
{% endhighlight %}

This is a great time to use features such as Template Strings in your code. In a follow up post, I'll talk about some ways you can use ES2015 in your code now even if you have to write legacy browser compliant code at the moment. Thanks for reading.

Stay Awesome.
