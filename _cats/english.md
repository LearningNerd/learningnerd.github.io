---
name: english
title: "Articles About English"
---

Here's a selection of my older blog posts about English language topics -- grammar, vocabulary, punctuation, oh my!

<div class="tiles">    
  {% for post in site.posts reversed %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->
