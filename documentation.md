---
layout: page
title: Documentation
children: doc
---
The first step to using the Mirin Template is to download and set up the files:
{% if true %}
<div class="post">
<a href="{{ "/getting-started" | prepend:site.baseurl }}"> <div class="button"> Download </div> </a>
</div>
{% endif %}
<div class="flex-container">
{% assign pages_list = site.pages | where: "layout", "doc" | sort: "section" %}
{% for doc in pages_list %}
{% if doc.subsection == 0 %}
<div class="post flex-object" >
<h1 class="{% if doc.incomplete %}incomplete {% endif %}post-title">
<a href="{{ doc.url | prepend:site.baseurl }}">{{ doc.title }}</a>
</h1>
{{ doc.content | markdownify }}
<a href="{{ doc.url | prepend:site.baseurl }}"><div class="button">Learn more</div></a>
</div>
{% endif %}
{% endfor %}
</div>

Bonus:
* [Learn Lua](https://www.lua.org/manual/5.1/)

Documentation by XeroOl, Chegg, Kirby5464
