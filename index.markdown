---
layout: blog                   
title: Blog
---
<p>
  {% for post in site.posts limit:5 %}
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <div>{{ post.content | strip_html | truncatewords: 75 }}</div>
    <em>Posted on {{ post.date | date_to_long_string }}.</em>
    <div><a href="{{ post.url }}#disqus_thread">View Comments</a></div>
  {% endfor %}
</p>
