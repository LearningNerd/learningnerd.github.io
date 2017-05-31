---
name: daily
title: "Daily Learning Notes"
---

First I made [**100 daily video blogs in 100 days**](/vlog/) to share what I'm learning -- both about myself and about the world -- as an experiment to fight my fears, gain self-acceptance, and channel my curiosity!

Now I'm experimenting with a daily blog post (sometimes with videos, images and other media) to document what I'm learning. These notes are the raw material from which I build my understanding:

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->

And you can see all of my previous daily video experiments from October and November 2015 <strong><a href="https://plus.google.com/u/0/collection/kAGMq">in this Google+ collection</a></strong>. (I hope to add them to my website in the near future. Sorry for the laziness!)