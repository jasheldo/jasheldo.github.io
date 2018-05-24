---
layout: page
title: I write stuff down. Some of it is worth reading.
tagline: I write stuff down. Some of it is worth reading.
---
{% include JB/setup %}
    
## Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


