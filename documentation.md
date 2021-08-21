---
layout: page
title: Documentation
children: doc
---
[Getting Started](getting-started)
<div class="flex-container">
{% assign pages_list = site.pages | where: "layout", "doc" | sort: "section" %}
{% for doc in pages_list %}
{% if doc.subsection == 0 %}
<div class="post flex-object" >
<h1 class="{% if doc.incomplete %}incomplete {% endif %}post-title">
<a href="{{ doc.url | prepend:site.baseurl }}">{{ doc.title }}</a>
</h1>
{{ doc.content | markdownify }}
<a href="{{ doc.url | prepend:site.baseurl }}">Learn more</a>
</div>
{% endif %}
{% endfor %}
<div/>

Bonus:
* [Learn Lua](https://www.lua.org/manual/5.1/)

Documentation by XeroOl, Chegg, Kirby5464
