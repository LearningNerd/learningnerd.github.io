---
layout: archive
permalink: /featured/
title: "Featured Videos"
---

My slightly more polished videos, including the first intro video (a new one will be up later!) and the start of my series on mathematical cognition.

<div class="tiles">
{% for post in site.categories.featured %}
	{% include post-list.html %}
{% endfor %}
</div><!-- /.tiles -->