---
layout: page-fullwidth
title:  "Roboty mobilne Mindstorm"
subheadline:  "Projekty"
teaser: "Opis zestawów Lego Mindstorms oraz specyfikacje przykładowych robotów."
breadcrumb: true
tags:
    - projects
    - finished
categories:
    - projects
image:
    thumb: "mindstorms/test1.jpg"
info:
    full: true
permalink: "/legomindstorms/"
---
<h3>Przykładowe roboty sumo</h3>
{% assign sorted_pages = (site.categories.legomindstorms) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for robot in sorted_pages %}
    {% if robot.tags contains 'legosumo' %}
    <li>
    <div style="font-size: 100%; font-weight: bold"><a href="{{ robot.url }}">{{ robot.title }}</a></div>    
    {% if robot.image.thumb %}
    <p><center><a href="{{ robot.url }}"/><img align="left" style="max-height: 150px; max-width: 200px" src="{{ site.urlimg }}/projects/{{ robot.image.thumb }}" /><br /></center></p>
    {% endif %}    
    </li>       
    {% endif %} 
    {% endfor %}
</ul>

<h3>Przykładowe roboty śledzące linię</h3>
{% assign sorted_pages = (site.categories.legomindstorms) %}
<ul class="small-block-grid-1 medium-block-grid-2 large-block-grid-3">
    {% for robot in sorted_pages %}
    {% if robot.tags contains 'followtheline' %}
    <li>
    <div style="font-size: 100%; font-weight: bold"><a href="{{ robot.url }}">{{ robot.title }}</a></div>    
    {% if robot.image.thumb %}
    <p><center><a href="{{ robot.url }}"/><img align="left" style="max-height: 150px; max-width: 200px" src="{{ site.urlimg }}/projects/{{ robot.image.thumb }}" /><br /></center></p>
    {% endif %}    
    </li>    
    {% endif %}    
    {% endfor %}
</ul>


Najistotniejszą kwestią podczas budowy robota mobilnego przeznaczonego do startu w zawodach jest platforma sprzętowa. Powinna ona umożliwiać szybkie stworzenie prototypu konstrukcji, ułatwiać jego późniejsze modyfikacje oraz być na tyle elastyczna, aby można było bez dużych nakładów czasowych oraz pieniężnych rozszerzać konstrukcję o dodatkowe elementy. Wszystkie te cechy spełniają zestawy z serii Lego Minstorms NXT. Jest to kolejna generacja nowatorskiej serii RCX, wprowadzona na rynek w roku 2006 a następnie rozszerzana i odświeżana. Zestawy z serii Mindsotrms łączą klocki Lego (głównie z serii Lego Technic) z czujnikami elektronicznymi, serwomechanizmami oraz komputerową jednostką centralną. Pozwala to na konstruowanie z nich robotów praktycznie dowolnej ich klasy.<br>

<p><center><img class="text-center" style="height: 350px" src="{{ site.urlimg }}projects/mindstorms/bricks.jpg"/></center></p>
<font size="2" color="gray"><center>Podstawowy zestaw elementów sterujących Lego NXT; a) komputer centralny, b) czujnik dotykowy, c) czujnik natężenia dźwięku, d) czujnik natężenia światła, e) dalmierz ultradźwiękowy, f) serwonapędy</center></font>

Klocki z tej serii zostały bardzo dobrze przyjęte nie tylko przez standardowych odbiorców firmy Lego (a więc dzieci i młodzież), zostały również szczególnie docenione przez placówki dydaktyczne i naukowe. W szkołach służą do nauki konstrukcji i programowania, dając uczniom bardzo pożądane sprzężenie od ich działań. Zaprogramowany układ funkcjonuje w rzeczywistości, a wyniki są namacalne (w przeciwieństwie do klasycznego podejścia, gdzie wyświetlenie czegoś jedynie na ekranie nie daje aż takiej satysfakcji). Nawet na poziomie uniwersyteckim uniwersalność i elastyczność struktury pozwala na prowadzenie badań naukowych z wielu dziedzin -- robotyki mobilnej, systemów wbudowanych, inżynierii oprogramowania.<br>

Podstawowe elementy zestawu NXT przedstawione są na rysunku \ref{fig:bricks}. Do komputera centralnego podłączyć można standardowo do 4 sensorów oraz 3 serwonapędy.<br>

Struktura sterownika jest elastyczna i uniwersalna, a duża część przetwarzania danych sensorycznych jest oddelegowana do samych czujników -- np. czujnik ultradźwiękowy zawiera wbudowany mikrokontroler przetwarzający pomiary, dzięki czemu centralny układ otrzymuje ostateczny wynik pomiaru, nie wymagający dalszej obróbki.<br>

Ponieważ rdzeń konstrukcji jest oparty o klocki Lego, możliwe jest bardzo szybkie zbudowanie prototypu i testowanie algorytmów sterowania oraz różnych ustawień sensorów, podczas równoległego tworzenia komponentów docelowego robota. Konstrukcje z Lego umożliwiają zmianę koncepcji w dowolnym momencie. W tym samym czasie zamiast dwóch iteracji (przy klasycznym projektowaniu i budowie konstrukcji specjalizowanej z elementów ogólnodostępnych) można ich wykonać kilkanaście, otrzymując w wyniku konstrukcję dużo bardziej dopracowaną i dogłębnie przetestowaną.<br>




