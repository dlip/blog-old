---
layout: blog                   
title: Blog
---
#Blog
<p>
  {% for post in site.posts limit:5 %}
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.content }}
    <em>Posted on {{ post.date | date_to_long_string }}.</em>
    <a href="{{ post.url }}#disqus_thread">View Comments</a>
  {% endfor %}
</p>
