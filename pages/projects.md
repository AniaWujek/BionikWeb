---
layout: page-fullwidth
show_meta: false
subheadline: "Team"
breadcrumb: true
title: "Projects"
teaser: "Our research activity"
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/projects/"
---
{% assign sorted_pages = (site.categories.project) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for project in sorted_pages %}
    {% if project.info.featured %}
    <li>
    <a href="{{ site.url }}{{ project.url }}"><img src="{{ site.urlimg }}/projects/{{ project.image.thumb }}" alt="" /></a>
    <div style="font-size: 150%; font-weight: bold">{{ project.title }}</div>
    <p style="font-size: 90%">{{ project.teaser }}</p>
    {% if project.info.full %}
    <div class="text-right"><a href="{{ site.url }}{{ project.url }}">More...</a></div>
    {% endif %}
    </li>
    {% endif %}
    {% endfor %}
</ul>

{% for i in (2007..2015) reversed %}
{{ i }}
----
<ul>
{% for post in sorted_pages %}
  {% capture year %}{{post.date | date: "%Y"}}{% endcapture %}
  {% assign yy = year | plus: 0 %}
  {% if i == yy %}
  <li>
    <p>{{ post.title }}</p>
    <p>{{ post.teaser }}</p>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}
