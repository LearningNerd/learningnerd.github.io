---
name: cant-even-tracker
title: "\"I can't even\" tracker app"
---

My ultimate goal is to transform every "I can't even" feeling into an "Actually I can!" feeling. As I wrote in my personal notes on [the day I started building this app]({% post_url 2017-08-08-notes %}), I have a lot of panic attacks and feelings of "I can't even" -- a meme-ified phrase that I like because it sounds funny and it perfectly captures the heart of the issue I have with these strong emotions and negative thoughts that I sometimes struggle with. After having a lot of success so far with my [social alarm clock app](/social-alarm-clock), I figured it couldn't hurt to build another app to track these "I can't even" feelings and see if having more quantitative data can help me debug my brain.

**Blog posts on building the "I can't even"/"Actually I can!" tracker app:**

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->
