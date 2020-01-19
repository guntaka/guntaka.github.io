---
layout: default
title: Guntaka Home
---
## Heading head
- list 1
- list 2
- list 3

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>