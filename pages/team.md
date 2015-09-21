---
layout: page-fullwidth
show_meta: false
subheadline: "Team"
breadcrumb: true
title: "Team"
teaser: "Meet our team members"
#header:
#image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/team/"
---
{% assign sorted_pages = (site.categories.team) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for member in sorted_pages reversed%}
    <li>
    <p><center><img class="text-center photo-round" style="height: 200px" src="{{ site.urlimg }}/team/{{ member.image.thumb }}" /><br /></center></p>
    <div><i>{{ member.info.title }}</i></div>
    <div style="font-size: 150%; font-weight: bold">{{ member.title }}</div>
    <p style="font-size: 90%">{{ member.teaser }}</p>
    {% if member.info.full %}
    <div class="text-right"><a href="{{ site.url }}{{ member.url }}">More...</a></div>
    {% endif %}
    </li>
    {% endfor %}
</ul>

