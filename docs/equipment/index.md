---
layout: default
title: Equipment
permalink: /docs/equipment/
has_children: true
nav_order: 2
---

# Equipment Index

Welcome to the equipment section. Below is a list of all available equipment:

<ul>
  {% for item in site.equipment %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
  {% endfor %}
</ul>
