---
layout: archive
permalink: /vlog/
title: "Daily Vlog Experiment"
---

From October 2015 to January 2016, I'm making 100 daily video blogs to share what I'm learning -- both about myself and about the world -- as an experiment to fight my fears, gain self-acceptance, and channel my curiosity.

<strong><a href="https://plus.google.com/u/0/collection/kAGMq">See all the previous vlogs here</a></strong>

(Pardon my laziness -- I will post all the old video blogs on this page soon. For now, they're all in my Google+ collection in the link above. Cheers!)

<div class="tiles">
{% for post in site.categories.vlog %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->