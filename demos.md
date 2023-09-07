---
layout: default
title: Demos
permalink: /demos/
hide_contact_cta: true
---
<div>
  <h1>{{page.title}}</h1>

  <div class="archive">
    <ul>
      {% for demo in site.demos limit:6 %}
          <li><div><strong><a class="demo-link" href="{{ demo.url | relative_url }}">{{ demo.title | escape }}</a></strong><br/></div></li>
          <li><div>More to come soon!</div></li>
      {%- endfor -%}
    </ul>
  </div>
</div>
