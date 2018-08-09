---
layout: default
title: Notes for HTML
permalink: "/html/"
---

<h1>{{ page.title }}</h1>

<ul>
  {% for html in site.html %}
    <li>
      <a href="{{html.url}}">{{html.title}}</a>
    </li>
  {% endfor %}
</ul>
