---
layout: article
title: "Some Things I Don't Know About JavaScript"
permalink: /2015/05/07/dont-know-javascript/
---

After all that time I spent figuring out the first practice problem on [**exercism.io**](http://exercism.io/) (see [yesterday's blog post]({% post_url 2015-05-06-exercism %})), I realized that I actually don't know all that much about JavaScript yet, despite everything I learned during my [30 Days of Web Dev challenge](http://learningnerd.github.io/30DaysOfWebDev/).

I just took a look at the [second exercism practice problem](http://exercism.io/exercises/javascript/word-count/readme), and I have no clue how to solve it! Here's the first thing I don't understand:

{% highlight js %}
var expectedCounts = { word: 1 };
{% endhighlight %}

Is this an array? An object? Why is `word` not in quotes like most strings usually are? Does that mean it's a property of an object? But then...

{% highlight js %}
var expectedCounts = { car: 1, ":": 2, carpet: 1, as: 1, java: 1, "javascript!!&@$%^&": 1 };
{% endhighlight %}

Why are some of these things in quotes and others aren't? And what about this:

{% highlight js %}
var expectedCounts = { testing: 2, 1: 1, 2: 1 };
{% endhighlight %}

I thought variable names couldn't begin with numbers. Are the rules different for properties of objects? Or are these array indexes?

And here's another thing I haven't learned yet, which I saw in the skeleton file for [my first exercism submission](http://exercism.io/submissions/2e4c326e2845434c9f37af0ad082290a):

{% highlight js %}
var Bob = function() {};

Bob.prototype.hey = function(input) {
    // Some more code in here
};
{% endhighlight %}

I don't actually know what a protoype is. I don't know how this is different from these other ways to define a method:

{% highlight js %}
// Another way to define this method:
var hey = function(input) {
    // Some more code in here
};

// And yet another way to define this method:
function hey(input) {
    // Some more code in here
}
{% endhighlight %}

Should I even be worrying about this yet? Is it important for me to understand this now, or is this one of those things that I'll gradually understand as I continue building things with JavaScript? Is it better to learn "by the book" or by getting my hands dirty? How do I find the right balance between the two?

Ugh, I hate it when I waste too much time fretting over the "best" way to learn something instead of just diving in and *learning* it!

*A more personal note/rant:* I meant to work on this some more today and start answering my questions, but that will have to wait until tomorrow because somehow it's already my bedtime. Oops. The day slipped away from me again, between meetup group stuff and chores and personal corespondences and my day job. I want to do better tomorrow, but I also don't want to beat myself up over not accomplishing as much as I wanted to today. I do seem to be more productive when I practice self-acceptance, so I'm making a point of doing that more again.