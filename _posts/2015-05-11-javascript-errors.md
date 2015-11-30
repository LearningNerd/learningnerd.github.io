---
layout: article
title: Throwing Errors in JavaScript
permalink: /2015/05/11/javascript-errors/
---

The [third JavaScript problem on exercism.io](http://exercism.io/exercises/javascript/hamming/readme) both intimidated and amused me: "Write a program that can calculate the Hamming difference between two DNA strands."

I had never heard of this thing, so I went to [Wikipedia](http://en.wikipedia.org/wiki/Hamming_distance) and found some more examples:

>The Hamming distance between:

>- "ka**rol**in" and "ka**thr**in" is **3**.
- "k**a**r**o**lin" and "k**e**r**st**in" is **3**.
- 10**1**1**1**01 and 10**0**1**0**01 is **2**.
- 2**17**3**8**96 and 2**23**3**7**96 is **3**.

I see it now. A very simple idea: line up the strings of characters, go through them one character at a time, and count each instance in which the characters *don't* match. Done!

The instructions have one more important note: "The Hamming distance is only defined for sequences of equal length." And the last test expects an error message if the two sequences are not the same length.

##Throwing Errors in JavaScript

I'm ashamed to admit that even after getting pretty comfortable with JavaScript last month during my [30 Days of Web Dev challenge](http://learningnerd.github.io/30DaysOfWebDev/), I never learned how to throw error messages! I don't even know why people call it "throwing" error messages. In my mind, that phrase conjures up funny mental images of computers literally throwing things at their users!

I starting skimming [chapter 8 of Eloquent JavaScript](http://eloquentjavascript.net/08_error.html) and found this part slightly helpful (but also a bit confusing because I skipped chapters 3, 4, 5, 6, and 7):

>"Exceptions are a mechanism that make it possible for code that runs into a problem to *raise* (or *throw*) an exception, which is simply a value. Raising an exception somewhat resembles a super-charged return from a function: it jumps out of not just the current function but also out of its callers, all the way down to the first call that started the current execution. This is called *unwinding the stack*."

The code examples from that chapter pointed me in the right direction (and gave me some syntax that I could copy-paste). So I think I can do something like this:

{% highlight js %}
// if the two DNA strands are of equal lengths
if (sequence1.length === sequence2.length) {
    // compare the Hamming difference here
} else {
    // if different lengths, throw an error
    throw new Error('DNA strands must be of equal length.';
}
{% endhighlight %}

Let's see if that code  passes the last test... Yay, it worked! Well, I clearly have *a lot* more to learn about error-handling in JavaScript, but this was a good way to get my feet wet.

#Comparing Strings (or DNA Strands)

To compute the Hamming difference of two strings, I think all I need to do is iterate through each character of the strings and see if they match. If they do match, great! If they don't match, then I need to count up how many chracters are different. The final count will be the Hamming difference.

When in doubt, I just use a for loop because it's compatible with older browsers and it's very straightforward:

{% highlight js %}
var HammingDifference = 0;
for (i = 0; i < sequence1.length; i++) {
    // if this character in the sequence doesn't match
    if (sequence1[i] != sequence2[i]) {
        // increase the HammingDifference
        HammingDifference++;
    }
}
return HammingDifference;
{% endhighlight %}

Let's see if that works... Yeah, it passed every test! This one was way too easy.

Well, it's time for me to do some chores, eat some food, and get ready to go to work. But if I have any downtime at the office, I'll do some more studying! And I hope to learn some more at the front-end web development [meetup group](http://www.meetup.com/LearnToCodeLA/) that I'm hosting tonight.