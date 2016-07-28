---
layout: page
title: Blog
permalink: /blog/
---

This blog will be used mainly for topics of academic interest, like LaTeX, R, Praat, etc.
I blog semi-regularly about more popular interest topics at [my blogger site](http://mountainmanlinguistics.blogspot.com).
A full listing of my blog posts follows below.

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>