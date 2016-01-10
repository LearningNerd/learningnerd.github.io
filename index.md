---
layout: archive
permalink: /
title:
---

<strong><em>On a mission to learn everything, sharing everything I learn!</em></strong>

Latest project: I made [**100 daily video blogs in 100 days**](/vlog/) to share what I'm learning -- both about myself and about the world -- as an experiment to fight my fears, gain self-acceptance, and channel my curiosity!

December 2015 was my [**math immersion month**](/math/), a daily video blog experiment to conquer my math anxiety and not only learn some math, but also learn to love it!

And you can see all of my previous daily video experiments <strong><a href="https://plus.google.com/u/0/collection/kAGMq">in this Google+ collection</a></strong>.

<h2>Featured Videos:</h2>
<div class="tiles">
{% for post in site.categories.featured %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->

<h2>All Blog Posts:</h2>
<div class="tiles">
{% for post in site.posts %}
    {% unless post.categories contains 'featured' %}
	{% include post-list.html %}
	{% endunless %}
{% endfor %}
</div><!-- /.tiles -->