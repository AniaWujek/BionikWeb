---
layout: page-fullwidth
show_meta: false
subheadline: ""
breadcrumb: true
title: "Aktualności"
teaser: ""
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/activities/"
---

Śledźcie nasze działania na naszym profilu na facebook'u: [KNR "Bionik"](https://www.facebook.com/KNR.Bionik){:target="_blank"}<br>

{% assign sorted_pages = (site.categories.activities) %}
<ul>
  {% for post in sorted_pages%}
    <li>
      <div style="font-size: 150%; font-weight: bold">{{ post.title }}</div>
      <div style="font-style: italic">{{ post.date | date: "%Y-%m-%d" }}</div>
      <p style="font-size: 90%">{{ post.teaser }}</p>
      <a href="{{ post.url }}">Więcej...</a>
      {% if post.image.thumb %}
       <p><center><img class="text-center photo-round" style="height: 200px" src="{{ site.urlimg }}/activities/{{ post.image.thumb }}" /><br /></center></p>
      {% endif %}
      
    </li>
  {% endfor %}
</ul>

