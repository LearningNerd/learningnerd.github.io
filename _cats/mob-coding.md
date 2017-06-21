---
name: mob-coding
title: "Mob Coding App"
---

**GitHub repo:** [https://github.com/LearnTeachCode/mob-coding](https://github.com/LearnTeachCode/mob-coding)

As a side project, I'm building a [turn-based mob programming web app](https://github.com/LearnTeachCode/mob-coding) for real-time collaboration on coding challenges. This early vesion of the app is meant to be used by in-person groups at programming meetups and classes, to serve as a warmup exercise or icebreaker activity.

**Learn About Mob Programming:**

  - [What is mob programming?](https://www.agilealliance.org/glossary/mob-programming/) by the Agile Alliance

  - Video: ["Mob Programming, A Whole Team Approach"](https://www.youtube.com/watch?v=8cy64qkgTyI) by Woody Zuill

  - Article: ["Introducing Mob programming: The best team technique you've (probably) never heard of"](http://www.infoworld.com/article/2941233/application-development/introducing-mob-programming-the-best-team-technique-youve-probably-never-heard-of.html) by Daniel P. Dern

  - [MobProgramming.org and the Mob Programming Conference](http://mobprogramming.org/)

**Mob Coding Blog Posts:**

Many of my [**daily learning notes**](/daily/) are partially or entirely focused on what I've been learning, experimenting, and struggling with as I'm building this app, so I decided to create a category just for this topic!

<div class="tiles">
  {% for post in site.posts %}
    {% if post.cats contains page.name %}
      {% include post-list.html %}
    {% endif %}
  {% endfor %}
</div><!-- /.tiles -->
