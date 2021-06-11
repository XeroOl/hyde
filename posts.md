---
layout: page
title: Posts
children: post
---
Here are all of the blog posts:
{% for post in site.posts %}
[{{post.title}}]({{post.url | prepend:site.baseurl}})
{% endfor %}
