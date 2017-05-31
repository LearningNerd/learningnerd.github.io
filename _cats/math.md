---
name: math
title: "Math Immersion Month"
---

My December 2015 project: see if I can not only (re)learn math but also learn to love it, and make a daily video to share the process!

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->