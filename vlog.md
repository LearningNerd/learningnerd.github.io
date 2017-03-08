---
layout: archive
permalink: /vlog/
title: "Daily Vlog Experiment"
---

From October 2015 to January 2016, I made 100 daily video blogs in 100 days to share what I'm learning -- both about myself and about the world -- as an experiment to fight my fears, gain self-acceptance, and channel my curiosity. December 2015 was my [**math immersion month**](/math/), a daily video blog experiment to conquer my math anxiety and not only learn some math, but also learn to love it!

## January 2016

<div class="tiles">
{% for post in site.categories.vlog %}
	{% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
	{% if year != "2017" %}
		{% include post-list.html %}
	{% endif %}
{% endfor %}
</div><!-- /.tiles -->

## December 2015

My December 2015 project: see if I can not only (re)learn math but also learn to love it, and make a daily video to share the process!

<div class="tiles">
{% for post in site.categories.math %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->

## October and November 2015

<a href="https://plus.google.com/u/0/collection/kAGMq">See all the previous vlogs here</a>

(Pardon my laziness -- I will post all the old video blogs on this page soon. For now, they're all in my Google+ collection in the link above.)