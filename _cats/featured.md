---
name: featured
title: "Featured Videos"
---

My slightly more polished videos, including the first intro video (a new one will be up later!) and the start of my series on mathematical cognition.

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->