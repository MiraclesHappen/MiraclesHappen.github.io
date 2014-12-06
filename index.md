---
layout: home
---

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{ post.gather_date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.gather_date | date:"%Y-%m-%d" }}">{{ post.gather_date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.index }} {{ post.title }}</a>
  </li>
{% endfor %}
</ul>
