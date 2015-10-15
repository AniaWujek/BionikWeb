---
layout: page-fullwidth
show_meta: false
subheadline: "Projekty"
breadcrumb: true
title: "Projekty"
teaser: ""
#header:
#   image_fullwidth: "headers/header_rubik_2.jpg"
permalink: "/projects/"
---
<h2>Aktualne projekty - potrzebni ludzie!</h2>
{% assign sorted_pages = (site.categories.projects) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for project in sorted_pages %}
    {% if project.tags contains 'finished' %}
    {% else %}
    <li>    
    {% if project.image.thumb %}
    <p><center><img class="text-center" style="height: 200px" src="{{ site.urlimg }}/projects/{{ project.image.thumb }}" /><br /></center></p>
    {% endif %}
    <div style="font-size: 150%; font-weight: bold">{{ project.title }}</div>
    <p style="font-size: 90%">{{ project.teaser }}</p>
    <a href="{{ project.url }}">Więcej...</a>
    </li>    
    {% endif %}    
    {% endfor %}
</ul>

<h2>Projekty ukończone</h2>
{% assign sorted_pages = (site.categories.projects) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for project in sorted_pages %}
    {% if project.tags contains 'finished' %}
    <li>    
    {% if project.image.thumb %}
    <p><center><img class="text-center" style="height: 200px" src="{{ site.urlimg }}/projects/{{ project.image.thumb }}" /><br /></center></p>
    {% endif %}
    <div style="font-size: 150%; font-weight: bold">{{ project.title }}</div>
    <p style="font-size: 90%">{{ project.teaser }}</p>
    <a href="{{ project.url }}">Więcej...</a>
    </li>    
    {% endif %}    
    {% endfor %}
</ul>
