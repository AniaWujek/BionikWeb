---
layout: page-fullwidth
title:  "Roboty mobilne Mindstorm"
subheadline:  "Roboty"
teaser: "Nie tylko do zabawy."
breadcrumb: true
tags:
    - projects
categories:
    - projects
image:
    thumb: "mindstorms/bricks.jpg"
info:
    full: true
---

Najistotniejszą kwestią podczas budowy robota mobilnego przeznaczonego do startu w zawodach jest platforma sprzętowa. Powinna ona umożliwiać szybkie stworzenie prototypu konstrukcji, ułatwiać jego późniejsze modyfikacje oraz być na tyle elastyczna, aby można było bez dużych nakładów czasowych oraz pieniężnych rozszerzać konstrukcję o dodatkowe elementy. Wszystkie te cechy spełniają zestawy z serii Lego Minstorms NXT. Jest to kolejna generacja nowatorskiej serii RCX, wprowadzona na rynek w roku 2006 a następnie rozszerzana i odświeżana. Zestawy z serii Mindsotrms łączą klocki Lego (głównie z serii Lego Technic) z czujnikami elektronicznymi, serwomechanizmami oraz komputerową jednostką centralną. Pozwala to na konstruowanie z nich robotów praktycznie dowolnej ich klasy.<br>

<p><center><img class="text-center" style="height: 350px" src="{{ site.urlimg }}projects/mindstorms/bricks.jpg"/></center></p>
<font size="2" color="gray"><center>Podstawowy zestaw elementów sterujących Lego NXT; a) komputer centralny, b) czujnik dotykowy, c) czujnik natężenia dźwięku, d) czujnik natężenia światła, e) dalmierz ultradźwiękowy, f) serwonapędy</center></font>

Klocki z tej serii zostały bardzo dobrze przyjęte nie tylko przez standardowych odbiorców firmy Lego (a więc dzieci i młodzież), zostały również szczególnie docenione przez placówki dydaktyczne i naukowe. W szkołach służą do nauki konstrukcji i programowania, dając uczniom bardzo pożądane sprzężenie od ich działań. Zaprogramowany układ funkcjonuje w rzeczywistości, a wyniki są namacalne (w przeciwieństwie do klasycznego podejścia, gdzie wyświetlenie czegoś jedynie na ekranie nie daje aż takiej satysfakcji). Nawet na poziomie uniwersyteckim uniwersalność i elastyczność struktury pozwala na prowadzenie badań naukowych z wielu dziedzin -- robotyki mobilnej, systemów wbudowanych, inżynierii oprogramowania.<br>

Podstawowe elementy zestawu NXT przedstawione są na rysunku \ref{fig:bricks}. Do komputera centralnego podłączyć można standardowo do 4 sensorów oraz 3 serwonapędy.<br>

Struktura sterownika jest elastyczna i uniwersalna, a duża część przetwarzania danych sensorycznych jest oddelegowana do samych czujników -- np. czujnik ultradźwiękowy zawiera wbudowany mikrokontroler przetwarzający pomiary, dzięki czemu centralny układ otrzymuje ostateczny wynik pomiaru, nie wymagający dalszej obróbki.<br>

Ponieważ rdzeń konstrukcji jest oparty o klocki Lego, możliwe jest bardzo szybkie zbudowanie prototypu i testowanie algorytmów sterowania oraz różnych ustawień sensorów, podczas równoległego tworzenia komponentów docelowego robota. Konstrukcje z Lego umożliwiają zmianę koncepcji w dowolnym momencie. W tym samym czasie zamiast dwóch iteracji (przy klasycznym projektowaniu i budowie konstrukcji specjalizowanej z elementów ogólnodostępnych) można ich wykonać kilkanaście, otrzymując w wyniku konstrukcję dużo bardziej dopracowaną i dogłębnie przetestowaną.<br>


<h3>Przykładowe roboty śledzące linię</h3>
<h4>Monia - Zespół: Katarzyna Mioduszewska i Dawid Dąbrowski </h4>

<h5>Konstrukcja</h5>

Robot zbudowany na podstawie prostego opisu z internetu. Dodatkowo, eksperymentowano z różnymi modelami kół oraz ich rozstawem, a także z pozycją czujnika natężenia światła odbitego, te trzy czynniki miały znaczący wpływ na efektywność pokonywania trasy.

<h5>Zasada działania i wyniki</h5>

Algorytm opierał się na regulatorze PID, z parametrami dobranymi na dokładne śledzenie linii i jak najmniejsze oscylacje. Niestety, dokładność nie była oceniana i robot przegrał z szybszymi, lecz mniej dokładnymi. Na trasie kwalifikacyjnej zastosowano modyfikację polegającą na zmianie algorytmu na gorzej wyregulowany, ale szybszy, która następowała po pokonaniu najostrzejszego zakrętu trasy. Niestety, nie było to wystarczające do awansu do finału.

<p><center><img class="text-center" style="height: 350px" src="{{ site.urlimg }}projects/mindstorms/monia.jpg"/></center></p>
<font size="2" color="gray"><center>Monia w trakcie przejazdu po planszy testowej</center></font>


<h4>Test1 - Zespół: Przemysław Łada i Michał Klimczak</h4>

<h5>Konstrukcja</h5>

Robot został zbudowany na zasadzie robota dwukołowego z napędem różnicowym. W odróżnieniu od klasycznego podparcia za pomocą koła sferycznego lub koła wleczonego(koła w wózkach sklepowych) zostały zastosowane podpory z odpowiednich klocków. Miało to na celu umożliwienie robotowi wykonywanie ruchów w dowolnej kolejności bez efektu koła wleczonego. Konstrukcja robota jest prosta i lekka, przez co robot nie dużego posiada momentu bezwładności i dobrze reaguje na zadany ruch. Dodatkowo środek ciężkości jest umiejscowiony bardzo blisko osi obrotu kół, dzięki czemu robot jest dobrze dociążony i ma dobrą przyczepność. Sensor został umieszczony na wysięgniku. Dzięki takiemu rozwiązaniu robot może skanować odpowiednio duży obszar przed sobą. Im dłuższy wysięgnik tym większa będzie prędkość kątowa i skanowany obszar. Długość wysięgnika została dobrana w taki sposób, aby badać dostatecznie duży obszar z odpowiednią prędkością kątową.
Cechy szczególne:
<ul>
<li>Prosta i lekka konstrukcja,</li>
<li>Środek ciężkości jest blisko osi kół co odpowiednio dociąża koła,</li>
<li>Jako podpory wykorzystane zostały odpowiednie klocki, dzięki temu robot może wykonywać dowolne manewry w dowolnej kolejności (brak efektu koła wleczonego),</li>
<li>Czujnik światła jest umieszczony na wysięgniku przez co omiata odpowiednio duży obszar.</li>
</ul>
<h5>Oprogramowanie</h5>

Robot porusza się przed siebie aż do momentu kiedy przestanie widzieć linię. Gdy się to stanie stara się ją ponownie znaleźć. Poszukiwanie linii składa się z trzech trybów szukania. Pierwszy tryb to obrót o 30 stopni w każdą stronę. Jest on oczywiście przerywany jeśli w trakcie robot natrafi na linię. W tym trybie obrót wykonywany jest z lekkim przesunięciem do przodu. Dzięki temu na lekkich zakrętach i gdy robot zgubi się na prostej, nie przestaje poruszać się do przodu. Gdy podczas tego trybu nie zostanie odnaleziona linia rozpoczyna się poszukiwanie w miejscu. Robot zatrzymuje się i obraca o kąt 110 stopni w każdą stronę. Tym razem nie przemieszcza się ponieważ silniki obracają się z taką samą prędkością, ale w przeciwne strony. Dzięki temu robot nie wypada z trasy podczas pokonywania trudnych fragmentów takich jak zakręt pod kątem prostym. Jest jeszcze ostatni awaryjny tryb poszukiwania używany gdy linia nie zostanie odnaleziona w dwóch poprzednich. Jest on identyczny jak tryb drugi z tym że robot obraca się o 180 stopni. Jest wykorzystywany gdy z powodu złego uwarunkowania np. omyłkowe przeoczenie linii, linia nie została odnaleziona. Gdy robot nie odnajdzie linii w tym trybie poddaje się i kończy działanie.


<p><center><img class="text-center" style="height: 350px" src="{{ site.urlimg }}projects/mindstorms/test1.jpg"/></center></p>
<font size="2" color="gray"><center>Robot Test1</center></font>

<h3>Przykładowy robot sumo - Orion</h3>
<h4>Zespół: Kinga Staszkiewicz, Karolina Borkowska i Kamila Lis</h4>

<h5>Konstrukcja</h5>

Orion to robot do walk sumo zbudowany z klocków Mindstorm. Początkowo ważył 2 kg i miał po dwa sensory światła(do lokalizacji końca planszy oznaczonej białym kolorem) i sensory ultradźwiękowe (do wykrycia przeciwnika). Dla wymagań lekkiej konkurencji Sumo w zawodach Bionikalia, zmniejszono jego wagę do 1 kg i ograniczono ilość czujników do jednego sensora danego rodzaju. Ograniczenia te były dość niekorzystne, ponieważ redukowały możliwość precyzyjnego ustawienia się wobec przeciwnika.<br>
Orion ma napęd na trzy silniki nisko usytuowane z tyłu, na przodzie opiera się na ,,pługu''. Dodatkowo przymocowano ruchomy pług, który opadał po pierwszym obrocie robota i wydłużał jego zasięg. Jego środek ciężkości był lekko przesunięty do tyłu, ale w momencie spychania przeciwnika przód był dociążany przez drugiego robota. Problem przesuniętego środka ciężkości, (który przyczyniał się do wywracania po podważeniu przez przeciwnika) chciałyśmy zredukować przez doczepienie z tyłu Oriona klapki blokującej upadek.

<h5>Oprogramowanie</h5>

Program sterujący robotem opiera się na poprzedniej wersji, zredukowany o odjęte czujniki. Robot przez pierwsze pięć sekund jest pasywny. Następnie obraca się w prawo wyszukując przeciwnika. Jeśli robot wykrył cel sprawdza czy nie wyjeżdża na białą obwódkę planszy. Jeśli tak to się cofa przez 1 sekundę, jeśli nie to atakuje przeciwnika. W przypadku zgubienia przeciwnika, robot znów obraca się w prawo skanując plansze w poszukiwaniu wroga.

<p><center><img class="text-center" style="height: 350px" src="{{ site.urlimg }}projects/mindstorms/orion.jpg"/></center></p>
<font size="2" color="gray"><center>Robot Orion</center></font>


