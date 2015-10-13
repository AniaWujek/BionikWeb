---
layout: page-fullwidth
show_meta: false
subheadline: "Projekty"
breadcrumb: true
title: "Projekty"
teaser: "Aktualne projekty, do których można (trzeba!) dołączać!"
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/projects/"
---
{% assign sorted_pages = (site.categories.projects) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for project in sorted_pages %}
    <li>    
    {% if project.image.thumb %}
    <p><center><img class="text-center photo-round" style="height: 200px" src="{{ site.urlimg }}/projects/{{ project.image.thumb }}" /><br /></center></p>
    {% endif %}
    <div style="font-size: 150%; font-weight: bold">{{ project.title }}</div>
    <p style="font-size: 90%">{{ project.teaser }}</p>
    <a href="{{ project.url }}">Więcej...</a>
    </li>
    {% endfor %}
</ul>
