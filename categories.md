---
layout: default
# title: 
# date: 2020-04-05
tagline: Topics and Posts List
# ref: 0
---

<div class = "container-fluid">
  <div class = "row justify-content-left">
  {{ site.bible }} => STUDY
  </div>
  <hr/>
  <li><a href="{{ site.baseurl }}/Mom-is-Free/">{{ "Mom is Free" }}</a>
    </li>
{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <a id="{{ category_name | slugize }}">
    {{ category_name }}
  </a>
  {% for post in site.categories[category_name] %}
    <li><a id="{{ post.title }}" href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
{% endfor %}
</div>
