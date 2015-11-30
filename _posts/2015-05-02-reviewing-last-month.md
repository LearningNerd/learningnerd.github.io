---
layout: article
title: Starting to Review What I Learned Last Month
permalink: /2015/05/02/reviewing-last-month/
---

I found some old notes in a document on my computer from day 1 of my [30 Days of Web Dev](http://learningnerd.github.io/30DaysOfWebDev/) challenge:

> Adding a slash at the front of a relative URL makes it relative to the root folder, not the current folder (I made a link to `/day1` but what I needed was `day1`)

And apprently I didn't know how to construct a relative URL that moves up one level, like `../day1` -- how did I not know that?! It's easy to forget that just a couple months ago, I had never even used the command line for anything. Now not only am I comfortable with navigating around the [file system](http://en.wikipedia.org/wiki/File_system), but I'm also comfortable with the basics of [Git](http://git-scm.com/) and I've even taught a couple [Learn to Code LA](http://www.meetup.com/LearnToCodeLA/) workshops about Git and [GitHub](http://github.com)!

Ugh, but I think I've already run out of time for this today, even though I've only spent like 20 minutes on this so far. It's been an unusual week, and the disruption of my daily routines really screws up my brain's normal [control flow](http://en.wikipedia.org/wiki/Control_flow), completely throwing me for a loop! (Hah, get it? For a loop! OK, I'm clearly sleep-deprived.)

##What I learned today:
- Practiced writing blog posts in [Markdown](http://en.wikipedia.org/wiki/Markdown)
  - Learned how to make blockquotes and nested lists in Markdown
- Checked if I still know how to solve [Fizz Buzz](http://en.wikipedia.org/wiki/Fizz_buzz), and I do!

Speaking of Fizz Buzz, [this solution](http://rosettacode.org/wiki/FizzBuzz#JavaScript) is much more elegant than mine was:

{% highlight js %}
var i, output;
for (i = 1; i < 101; i++) {
  output = '';
  if (!(i % 3)) output += 'Fizz';
  if (!(i % 5)) output += 'Buzz';
  console.log(output || i);
}
{% endhighlight %}

##Ideas for tomorrow:
*Copied from yesterday:*

- Learn more about Jekyll so I can customize this blog some more! Maybe add some metadata to track along with my blog posts, like how much time I spend learning about web dev each day.
- Do a thorough review of my 30-day challenge for April and write about what I learned.
- Finally do some background reading on the web itself, because I don't have a thorough understanding of its history or how it works.

And:

- A random idea-picker script to combat my indecisiveness every time I sit down to work on learning about web development! (Today I procrastinated all day long, unsure of what sort of project to start on next.)