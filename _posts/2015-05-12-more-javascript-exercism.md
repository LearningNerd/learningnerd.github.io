---
layout: article
title: More Exercism.io JavaScript Challenges
permalink: /2015/05/12/more-javascript-exercism/
---

I've been keeping detailed notes in this blog for all the [exercism.io](http://exercism.io/) problems that I've solved so far, but I don't want to give away the answers to *all* the practice problems! Besides, they're getting a little repetitive now, and much of what I'm doing is just review. So I'll only keep notes on the new things that I've learned. If a particularly new or challenging problem comes up, then maybe I'll blog about it in detail.

I started on [exercism.io challenge four](http://exercism.io/exercises/javascript/hamming/readme), but I haven't finished it yet. So far it's been a good challenge! First, I learned what's apparently called **literal notation** or **initializer notation** for [initializing objects in JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer):

{% highlight js %}
var myObject = {
    myProperty: someValue,
    myMethod: function(argument) {
        // do stuff        
    }
};
{% endhighlight %}

But I didn't end up using that notation, because I find object constructor notation to be much easier to read:

{% highlight js %}
function MyObject () {
    this.myProperty = someValue;
    this.myMethod = function(argument) {
        // do stuff        
    };
}
{% endhighlight %}

See this [overview of JavaScript objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) for more details on the different ways to define objects.

Second, I learned how to convert a string into an array of the string's characters using the [split() method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split):

{% highlight js %}
var myString = "blah!";
console.log(myString.split(''));
// output: [ "b", "l", "a", "h", "!" ]
{% endhighlight %}

I also learned how to use the [forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) method for the first time! It's just more compact than a `for` loop when you want to run a function on each element of an array.
 
And I re-learned how to use the [break](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/break) and [continue](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/continue) statements to change the flow of a loop by either terminating the loop entirely or skipping ahead to its next interation.

I also learned how to use the [arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments) to create a function that can take different kinds of inputs. Along with the [isArray()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray) method and the [typeof operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof), I can use this to create a function that can take either a string or an array as its input!

I *really* thought I could finish this problem before the end of the day, but I ran out of time. Tomorrow I'll get it working for sure!