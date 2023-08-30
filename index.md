---
layout: home
title: Welcome to Gopz Consulting
---

# Problem Solvers

Whether you have a project in the works that needs additional support or a vision translated into brass tax, Gopz Consulting can help. Founder, Ryan Collins, has spent the past decade on the front lines of a rapidly changing tech landscape, solutioning everything from low level, niche services to high level process architecture. He has engineered products that work for companies that know how to use them, including the world’s largest telemedicine provider, Teladoc Health. For any problem there are many roads to resolution. Together we’ll choose the road that works for you and ultimately improves your bottom line.

<div class="archive">
{% for post in site.posts limit:6 %}
  <article class="article">
    <a class="post-link" href="{{ post.url | relative_url }}"><img src="{{ post.image }}" class="thumb" /></a>
    <div><strong><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></strong><br/>
    {{ post.excerpt }}<br/><br/>
    </div>
  </article>
  {%- endfor -%}
</div>

