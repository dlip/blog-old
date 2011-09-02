---
layout: blog                   
title: Blog
---
<p>
  {% for post in site.posts limit:5 %}
    <div style="float:right"><a href="{{ post.url }}#disqus_thread">View Comments</a></div>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <em>Posted on {{ post.date | date_to_long_string }}.</em>
    <div>{{ post.content | strip_html | truncatewords: 75 }}</div>
    <div><a href="{{post.url}}">Read more...</a></div>
  {% endfor %}
</p>
