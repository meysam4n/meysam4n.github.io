---
layout: default
title: Home
---

# Welcome to My Jekyll Site
This site is powered by **Jekyll** and hosted on **GitHub Pages**.

Check out my [About page](about.html) or read my first blog post below.
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small> - {{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
