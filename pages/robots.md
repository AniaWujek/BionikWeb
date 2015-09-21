---
layout: page-fullwidth
show_meta: false
subheadline: "What a robotic team would be without the..."
breadcrumb: true
title: "Robots"
teaser: ""
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/robots/"
---
{% assign sorted_pages = (site.categories.robots) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for robot in sorted_pages %}
    <li>
    <p><center><img class="text-center radius" src="{{ site.urlimg }}/robots/{{ robot.image.thumb }}" /><br /></center></p>
    <div style="font-size: 150%; font-weight: bold">{{ robot.title }}</div>
    <p style="font-size: 90%">{{ robot.teaser }}</p>
    {% if robot.info.full %}
    <div class="text-right"><a href="{{ site.url }}{{ robot.url }}">More...</a></div>
    {% endif %}
    </li>
    {% endfor %}
</ul>

