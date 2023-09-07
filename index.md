---
layout: home
title: Welcome to Gopz Consulting
---

# Proven Experts in Building Apps and Standalone Services 

Whether you have a project in the works that needs additional support or a vision translated into brass tacks, Gopz Consulting can help. Founder, Ryan Collins, spent the past decade on the frontlines of a rapidly changing tech landscape, solutioning everything from low-level, niche services to high level process architecture. He engineered products that work for companies that know how to use them, including the world’s largest telemedicine provider, Teladoc Health. For any project there are many roads to completion. Together we’ll choose the path that works for you and ultimately improves your bottom line.

> ### What We Do in a Nutshell
> * Web and Mobile Applications
> * Standalone Microservices
> * AI Driven Applications

## Latest blog posts

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

