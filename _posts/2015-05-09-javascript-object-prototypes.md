---
layout: article
title: A Look at JavaScript Object Prototypes
permalink: /2015/05/09/javascript-object-prototypes/
---

Here's a question I haven't answered yet: what is a protoype? The other day, when I reviewed a couple of the [things I don't know about JavaScript]({% post_url 2015-05-07-dont-know-javascript %}), I shared my confusion about this example from [my first exercism.io practice problem](http://exercism.io/submissions/2e4c326e2845434c9f37af0ad082290a):

{% highlight js %}
var Bob = function() {};

Bob.prototype.hey = function(input) {
    // Some code in here
};
{% endhighlight %}

Yeah, that looks weird to me. Here's how I'm used to defining methods for my objects:

{% highlight js %}
Bob.hey = function(input) {
    // Some more code in here
};
{% endhighlight %}

What's the difference? Does it matter? Is it important for me to understand this yet, or should I put this question aside for now?

I didn't carve out much time for web dev studying today, but I couldn't resist looking ahead to [chapter 6 of Eloquent JavaScript](http://eloquentjavascript.net/06_object.html), which says this:

>"A prototype is another object that is used as a fallback source of properties. When an object gets a request for a property that it does not have, its prototype will be searched for the property, then the prototype’s prototype, and so on."

Hmm, OK then. That sort of makes sense. Apparently every (or almost every?) JavaScript object gets certain properties and methods from "the great ancestral" `Object.prototype` -- for example, it provides every object with the `toString` method, "which converts an object to a string representation."

Here's another important point from [Eloquent JavaScript](http://eloquentjavascript.net/06_object.html):

>"A prototype can be used at any time to add new properties and methods to all objects based on it."

Ah, maybe that's the key I've been looking for! So you can define a class of objects with certain properties and methods, create instances of those objects, and *later* add or change properties or methods for *all* of those objects by modifying their prototype. I'll have to try it out for myself with a few different examples to check my understanding. (But I'm feeling really sleepy now, which makes me averse to writing code, even though I can easily keep reading articles and jotting down my notes in here. So I'll come back to the coding another day, hopefully in the morning.)

Oh, and I think I answered one of my other questions from [the other day]({% post_url 2015-05-07-dont-know-javascript %}) in which I was very confused by these unknown things -- and I just discoverd that those things are object properties! Apparently object properties are exempt from the rules of variable naming; they can be named as numbers or even as strings!

As Haverbeke explains in [chapter 4 of Eloquent JavaScript](http://eloquentjavascript.net/04_data.html):

>"One way to create an object is by using a curly brace notation. [...] Inside the curly braces, we can give a list of properties separated by commas. Each property is written as a name, followed by a colon, followed by an expression that provides a value for the property. [...] Properties whose names are not valid variable names or valid numbers have to be quoted."

>{% highlight js %}
var descriptions = {
    work: "Went to work",
    "touched tree": "Touched a tree"
};
{% endhighlight %}

The example makes more sense in context, because the chapter is about a weresquirrel, a guy who sometimes turns into a squirrel, who keeps a daily log to try to identify which activities cause his squirrelfication. It's an awesome chapter, because it even dives into calculating correlations, which is something I've been wanting to (re)learn for a while now! (I'm not a weresquirrel, but I keep daily logs with the hope of identifying correlations to improve my day-to-day life.)

Anyway, that's a tangent for another time. **Lesson learned:** object properties can be named pretty much anything you want! And all objects inherit properties and methods from their prototypes. There's much more to learn, but I think now I might know just enough to tackle the [next exercism.io practice problem](http://exercism.io/exercises/javascript/word-count/readme)! Maybe I can give that a try tomorrow.