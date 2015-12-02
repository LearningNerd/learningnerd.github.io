---
layout: archive
permalink: /
title:
---

<strong><em>On a mission to learn everything, sharing everything I learn!</em></strong>

My next project will be a <em>math immersion month</em> with daily videos in December 2015! Yay math! Let's see if I can conquer my math anxiety and not only learn some math, but also learn to love it!

<div class="tiles">
{% for post in site.categories.math %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->

<strong><a href="https://plus.google.com/u/0/collection/kAGMq">See my previous daily video experiments here</a></strong>.

<h2>Featured Videos:</h2>
<div class="tiles">
{% for post in site.categories.featured %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->

<h2>Old Blog Posts:</h2>
<div class="tiles">
{% for post in site.posts %}
    {% unless post.categories contains 'featured' %}
	{% include post-list.html %}
	{% endunless %}
{% endfor %}
</div><!-- /.tiles -->
