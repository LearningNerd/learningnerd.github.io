---
layout: archive
permalink: /vlog/
title: "Daily Vlog Experiment"
---

In October and November 2015, I made a daily video blog as an experiment to fight my fears, gain self-acceptance, and channel my curiosity.

<strong><a href="https://plus.google.com/u/0/collection/kAGMq">See all the vlogs here</a></strong>

(Pardon my laziness -- I will post all the old video blogs on this page soon. For now, they're all in my Google+ collection in the link above. Cheers!)

<div class="tiles">
{% for post in site.categories.vlog %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->