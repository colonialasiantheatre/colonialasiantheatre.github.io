---
layout: default
title: Student Works
---

<ul class="nav">
  {% assign sorted_categories = site.categories | sort %}
  {% for category in sorted_categories reversed %}
    <li class="nav_item">
      <a class="nav_link tab_link" onclick="open_tab(event, '{{ category[0] | downcase |  replace: " ", "-" }}')">{{ category[0] }}</a>
    </li>
  {% endfor %}
</ul>

<div class="all-posts tab_content" markdown="1">
  <br>
  {% for post in site.posts %}
  -  [{{ post.title }}]({{ post.url }}) ({{ post.author }})
  {% endfor %}
</div>

{% for category in site.categories %}
{% assign category_id = category[0] | downcase |  replace: " ", "-" %}

<div class="{{ category_id }} tab_content" markdown="1">
## {{ category[0] }}
![](/assets/{{ category_id }}.jpg){: style="margin: 0 auto;"}
</div>

{% endfor %}

{% for category_citation in site.data.citation_img %}

<div class="{{ category_citation.name }} tab_content" style="text-align: right; font-size: 80%;" markdown="1">
{% assign citation = category_citation.citation %}
{{ citation }}
</div>
{% endfor %}

<br>

{% for category in site.categories %}

{% assign category_id = category[0] | downcase |  replace: " ", "-" %}
<div class="{{ category_id }} tab_content" markdown="1">
  {% assign sorted_posts = category[1] | sort %}
  {% for post in sorted_posts %}
  -  [{{ post.title }}]({{ post.url }}) ({{ post.author }})
  {% endfor %}
</div>

{% endfor %}

{% include nav_tab_script.html %}
