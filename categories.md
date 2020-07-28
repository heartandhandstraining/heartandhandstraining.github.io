---
layout: default
# title: 
# date: 2020-04-05
tagline: Topics and Posts List
# ref: 0
---

<div class = "container-fluid">
  <div class = "row justify-content-left">
    <a title="Certified Nurse Aide -Related posts" href="#CNA">CNA</a>,&nbsp;
    <a title="Web Development & Networking -Related posts" href="#WEB">WEB</a>,&nbsp;<a title="God and Faith-related posts" href="#GOD">GOD</a>,&nbsp;
    <a title="Free Online Bible" href="https://www.jw.org/en/library/bible/study-bible/books/" target="_blank">
      (BIBLE)
    </a>
  </div>
  <hr/>
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
  <span id="GOD">GOD CNA</span>
  <li><a href="{{ site.baseurl }}/Mom-is-Free/">{{ "Mom is Free" }}</a>
  </li>
</div>
