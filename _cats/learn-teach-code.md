---
name: learn-teach-code
title: "Learn Teach Code: Documenting My Journey"
---

My main projects for 2017 all revolve around **<a href="http://learnteachcode.org/">Learn Teach Code</a>**, the meetup group I started in 2015. This is by far the most ambitious, scary, but also rewarding and fulfilling project I've ever worked on! So I figured I'd better share the journey. I want to openly share my own learning process and all the ups and downs along the way.

For **March 2017**, my newest (and craziest!) project is to start **my own programming bootcamp**, first with a four-week part-time pilot program introducing full-stack JavaScript development. I want to create a truly valuable experience for my future students and dedicate myself to this full-time! But I'm also still struggling with my own personal challenges. So I want to share what happens, whether this ends up a spectacular success or a spectacular failure. Either way, it will be a great learning experience!

**Here are all my blog posts and video blogs for this project so far:**

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->