---
name: social-alarm-clock
title: "Social Alarm Clock App (Working Title: \"Wake Up, Liz!\")"
---

Even though I'm a morning person, I sometimes have a lot of trouble with the process of *actually waking up*. So as yet another side project, my social alarm clock app harnesses the power of technology and crowdsourcing to generate some early-morning motivation!

I'll add more details, backstory, and background information here over time. (I just created this page on Wednesday, July 26th, 2017.)

**Blog Posts on Building My Social Alarm Clock App:**

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->
