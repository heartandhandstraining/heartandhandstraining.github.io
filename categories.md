---
layout: page
# title: All
# date: 2020-04-05
tagline: Topics and Posts Lists
# ref: 0
---

<div class = "container-fluid">
  <div class = "row justify-content-left">
    <a title="Certified Nurse Aide -Related posts" href="#CNA">CNA</a>,&nbsp;<a title="Web Development & Networking -Related posts" href="#WEB">WEB</a>,&nbsp;<a title="God and Faith-related posts" href="#GOD">GOD</a>,&nbsp;<a title="Fiber Arts and Viking Sheep posts" href="#VSA">VSA</a>
  </div>
  <hr/>
  <!-- GOD
  <li><a id="mom-is-free" href="{{ site.url }}/Mom-is-Free/">{{ "Mom is Free" }}</a>
  </li> -->
{% for category in site.categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %}
  <a id="{{ category_name | slugize }}">
    {{ category_name }}
  </a>
  {% for post in site.categories[category_name] %}
    <li><a id="{{ post.title }}" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
{% endfor %}
  CNA GOD
  <li><a id="mom-is-free" href="{{ site.url }}/Mom-is-Free/">{{ "Mom is Free" }}</a>
  </li>
</div>
