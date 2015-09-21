---
layout: page-fullwidth
show_meta: false
subheadline: ""
breadcrumb: true
title: "activities"
teaser: ""
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/activities/"
---
{% assign sorted_pages = (site.categories.activities) %}
<ul>
  {% for post in sorted_pages reversed%}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

