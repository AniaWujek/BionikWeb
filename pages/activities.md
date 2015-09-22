---
layout: page-fullwidth
show_meta: false
subheadline: ""
breadcrumb: true
title: "Activities"
teaser: ""
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/activities/"
---

{% assign sorted_pages = (site.categories.activities) %}
<ul>
  {% for post in sorted_pages%}
    <li>
      <div style="font-size: 150%; font-weight: bold">{{ post.title }}</div>
      {{ post.excerpt }}
      <a href="{{ post.url }}">Read more...</a>
      {% if post.image.thumb %}
       <p><center><img class="text-center photo-round" style="height: 200px" src="{{ site.urlimg }}/activities/{{ post.image.thumb }}" /><br /></center></p>
      {% endif %}
      
    </li>
  {% endfor %}
</ul>

