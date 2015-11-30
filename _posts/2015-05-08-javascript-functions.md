---
layout: article
title: Reviewing JavaScript Functions
permalink: /2015/05/08/javascript-functions/
---

Yesterday I just reviewed a couple of the [things I don't know about JavaScript]({% post_url 2015-05-07-dont-know-javascript %}), but I didn't get around to answering any of my own questions yet. So today feels like a good day to get back to reading [**Eloquent JavaScript**](http://eloquentjavascript.net/), an excellent free book written by Marijn Haverbeke. I left off on [Chapter 3](http://eloquentjavascript.net/03_functions.html), which is all about functions.

##Functions in a Nutshell

I love Haverbeke's description of a function as **"a piece of program wrapped in a value"** to be used and reused later. But the [mathematical definition of a function](http://en.wikipedia.org/wiki/Function_(mathematics)) that I learned in school still applies: "a relation that associates an input to a single output according to some rule."

![Illustration of a function as a machine or black box]({{ site.url }}/images/functionmachine.png)

A function is often described as a [black box](http://en.wikipedia.org/wiki/Black_box) that turns one thing into another thing. Once the black box has been created, we can safely ignore its inner workings and focus instead on its inputs and outputs, treating the black boxes as building blocks to create more complex systems while keeping them modular and [extensible](http://en.wikipedia.org/wiki/Extensibility).

So that's all well and good. I feel pretty comfortable with the general idea of functions, and I got some good practice writing my own functions in JavaScript during my [30 Days of Web Dev](http://learningnerd.github.io/30DaysOfWebDev/) challenge. But there are still many details that I don't understand.

##Two Ways to Define Functions in JavaScript

[Yesterday]({% post_url 2015-05-07-dont-know-javascript %}) I noted my confusion over the different ways to define functions:

{% highlight js %}
// One way to define a function:
var hey = function(input) {
    // Some more code in here
};

// Another way to define a function:
function hey(input) {
    // Some more code in here
}
{% endhighlight %}

So I read through more of [Chapter 3 in Eloquent JavaScript](http://eloquentjavascript.net/03_functions.html), and I found that Haverbeke calls the first version a **"function definition"** and the second version a **"function declaration"**.

And according to [this StackOverflow post](http://stackoverflow.com/a/22173438), the first version (or function definition) is also called an **"anonymous function expression"**. Whew, what a mouthful of vague terms!

Anyhow, the most important difference between the two can be summed up with one word: [**hoisting**](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting). Another excellent book called [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20&%20closures/ch4.md) has a great chapter on hoisting, with the following example:

{% highlight js %}
a = 2;

var a;

// You'd think this would output "undefined":
console.log( a );

// But nope! The output will be "2"!

{% endhighlight %}

As [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20&%20closures/ch4.md) says, "There's a temptation to think that all of the code you see in a JavaScript program is interpreted line-by-line, top-down in order", but that's not always true! In JavaScript, declarations are hoisted to the top before the rest of the code is executed. "That means that you are able to use a function or a variable before it has been declared," says the [MDN Glossary](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting).

The above example illustrates the hoisting of the variable declaration; now here's an example of hoisting a *function* declaration, as illustrated in [Eloquent JavaScript](http://eloquentjavascript.net/03_functions.html):

{% highlight js %}
console.log("The future says:", future());

function future() {
  return "We STILL have no flying cars.";
}
{% endhighlight %}

The above code works because declarations are run before the rest of the code. As Haverbeke writes, "This is sometimes useful because it gives us the freedom to order code in a way that seems meaningful, without worrying about having to define all functions above their first use."

He also warns not to use function declarations inside conditional blocks or loops, because browsers don't handle it consistently and so things are likely to break! I'll definitely try to remember that.

Hurray, I now (sort of) understand the difference between function definitions and function declarations!

But in answering that one question, I've uncovered many more!

##New Questions:

- **What is variable scope?** The word "scope" appears in every article I read about "hoisting", so I better figure out what it means!
- **What's the difference between a statement and an expression?** I don't fully understand either of those terms.
- **What are all the *other* ways of defining functions in JavaScript, and how are they all different?** For example, I came across the term "named function expression" and a few other weird things.
- **How do JavaScript engines actually work, anyhow?** I think the "engine" is what compiles the JavaScript and runs the code, but I don't know the first thing about compilers. Or engines. (Not even combustion engines).

I have plenty more questions, but it's Friday and I want to do some other fun stuff tonight! So I think I'll give my brain some time to digest what I read today.