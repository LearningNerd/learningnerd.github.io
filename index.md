---
layout: archive
permalink: /
title:
---

<strong><em>On a mission to learn everything, sharing everything I learn!</em></strong>

**Current projects:**

  - In 2017, my main projects all revolve around <a href="http://learnteachcode.org/">Learn Teach Code</a>, the meetup group I started in 2015. I'm [**documenting my learning process here**](/learn-teach-code/) as I work on creating my own programming bootcamp.

**Previous projects:** 

  - I made [**100 daily video blogs in 100 days**](/vlog/) to share what I'm learning -- both about myself and about the world -- as an experiment to fight my fears, gain self-acceptance, and channel my curiosity!
  - December 2015 was my [**math immersion month**](/math/), a daily video blog experiment to conquer my math anxiety and not only learn some math, but also learn to love it!

<h2>Featured Videos:</h2>
<div class="tiles">
{% for post in site.categories.featured %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->

<h2>Archive of Some of My Old Blog Posts:</h2>
<div class="tiles">
{% for post in site.posts %}
    {% unless post.categories contains 'featured' %}
	{% include post-list.html %}
	{% endunless %}
{% endfor %}
</div><!-- /.tiles -->