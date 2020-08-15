---
layout: default
title: Student Works
---

<ul class="nav">
  {% assign sorted_categories = site.categories | sort %}
  {% for category in sorted_categories reversed %}
    <li class="nav_item">
      <a class="nav_link tab_link" id="{% if category[0] == "Hong Kong" %}default_active{% endif %}" onclick="open_tab(event, '{{ category[0] | downcase |  replace: " ", "-" }}')">{{ category[0] }}</a>
    </li>
  {% endfor %}
</ul>

{% for category in site.categories %}
<div id="{{ category[0] | downcase |  replace: " ", "-" }}" class="tab_content" markdown="1">
##  {{ category[0] }}
  {% assign sorted_posts = category[1] | sort %}
  {% for post in sorted_posts %}
  -  [{{ post.title }}]({{ post.url }}) ({{ post.author }})
  {% endfor %}
</div>
{% endfor %}

{% include nav_tab_script.html %}
