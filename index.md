---
layout: archive
permalink: /
title:
---

<strong><em>On a mission to learn everything, sharing everything I learn!</em></strong>

My current project: I'm making 100 daily video blogs to share what I'm learing -- both about myself and about the world -- as an experiment to fight my fears, gain self-acceptance, and channel my curiosity!

**Newest Daily Learning Vlogs:**

<div class="tiles">
{% for post in site.categories.vlog %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->

December 2015 was my [*math immersion month*](/math/) -- a daily learning and video blog experiment to conquer my math anxiety and not only learn some math, but also learn to love it! [**See all the math videos here.**](/math/)

<strong><a href="https://plus.google.com/u/0/collection/kAGMq">And all of my previous daily video experiments are here</a></strong>.

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