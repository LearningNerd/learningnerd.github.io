---
layout: article
title: JavaScript Word Count Challenge
permalink: /2015/05/10/javascript-word-count/
---

Today I'm going to try to solve the [second exercism.io JavaScript practice problem](http://exercism.io/exercises/javascript/word-count/readme).

At first I was [scared to tackle this problem]({% post_url 2015-05-07-dont-know-javascript %}), but after I answered a couple of my own questions about JavaScript objects [yesterday]({% post_url 2015-05-09-javascript-object-prototypes %}), and now I think I might be ready to tackle this problem.

The challenge: "Write a program that given a phrase can count the occurrences of each word in that phrase." My code needs to return an object that has one property for each word in the phrase, and each property's value should contain the word count.

{% highlight js %}
// input: "one fish two fish red fish blue fish"

// output should be:
var expectedCounts = { one: 1, fish: 4, two: 1, red: 1, blue: 1 };
{% endhighlight %}

So, where do I start? Hmm.

##Splitting Strings

Well, the first thing that comes to mind is that I need to chop up the phrase and get words separated by spaces. How do I do that? Let's ask the internet!

Ah, here's what I need: the [split() method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split), which splits a string object into an array. For example:

{% highlight js %}
var input = "one fish two fish red fish blue fish";
var arrayOfWords = input.split(' ');
// output: ["one", "fish", "two", "fish", "red", "fish", "blue", "fish"]
{% endhighlight %}

Now, how do I split a string using not just spaces as separators, but also tabs or newline characters? I have a feeling I'll need a [regular expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)... 

Yup, I do. The special character `\s` will match any white space character. Cool! And to account for multiple whitespace characters, I can just use `\s+` since the `+` character matches the preceding character (in this case, white space) if it occurs 1 *or more* times. So I should be able to do this:

{% highlight js %}
var input = "one    fish two\nfish red\t\tfish blue fish";
var arrayOfWords = input.split(/\s+/);
// output: ["one", "fish", "two", "fish", "red", "fish", "blue", "fish"]
{% endhighlight %}

Great, I have an array of words! That wasn't so hard, since I have used regular expressions before. (It was many years ago, back when I dabbled in PHP, but it seems that programming is a bit like riding a bike; you never forget it completely.)

##Counting Words and Creating an Object

Next, I need to do things: 1) count the instances of each word, and 2) convert this array into a list of properties within an object. I think these two things will happen at the same time, and I think I need a loop to iterate through my array of words. Something like:

{% highlight js %}
// arrayOfWords is ["one", "fish", "two", "fish", "red", "fish", "blue", "fish"]

// the wordCounts object will contain a property named for each word, with its count as the value
var wordCounts = {};

for (i = 0; i < arrayOfWords.length; i++) {
    // code to count words and create them as properties in the wordCounts object
}
{% endhighlight %}

But that code is just an empty shell; I need to give it some guts! After thinking about it for a while, I decided to try this:

{% highlight js %}
for (i = 0; i < arrayOfWords.length; i++) {
    var word = arrayOfWords[i];
    // if this word is not already a property of the wordCounts object, create it with the value of 1
    if (!wordCounts[word]) {
        wordCounts[word] = 1;
    } else {
    // if this word IS already a property of wordCounts, then increase its count value
        wordCounts[word]++;
    }
}
{% endhighlight %}

Let's see if that works... Woohoo! It mostly works! The only problem is that it fails the last test; it doesn't handle reserved words like `prototype` and `toString`. Hmm. Tricky, tricky!

Thankfully, I learned a bit about object prototypes in [yesterday's blog post]({% post_url 2015-05-09-javascript-object-prototypes %}), so at least this isn't *completely* foreign to me. Yesterday I learned that every object inherits certain properties and methods from an "ancestral" object prototype.

What I *didn't* know, which I learned just now by looking at other people's submissions on [exercism.io](http://exercism.io/), is that you can create objects without prototypes! It's a bit like a magic trick:

{% highlight js %}
// creates an object with no prototype and no inherited properties or methods
var wordCounts = Object.create(null);
{% endhighlight %}

And just like that, [problem solved](http://exercism.io/submissions/9a61b9e652a345158600f86cab5f4e51)! Hurrah!

Now that I think about it, I remember that [Eloquent JavaScript](http://eloquentjavascript.net/06_object.html) *did* cover creating objects without prototypes in [chapter 6](http://eloquentjavascript.net/06_object.html), but I only skimmed over it so I didn't really pay attention to that part.

Well, I could do more tonight, but I really want to relax and spend some time with my family since it's Mother's Day. I've been feeling somewhat sad today, since this is the first Mother's Day without my mom; she passed away last year. But I'm also celebrating her life and how much she influenced me. And I'm thinking about how I can make the most of what I've learned from her, and how I can live my life in a way that would make her proud.