# RF paikannimet
Finnish: Maanmittauslaitoksen paikannimirekisteristä lokakuussa 2024 haetut paikannimet ja satunnaismetsäluokittelija-scripti R-kielellä
English: Place names of the Place Name Register from National Land Survey of Finland October 2024 and a random forest classifier script in R

## NOTE TO READERS:
Repository in under construction and contains only the description in Finnish at the moment.

## Tausta
Paikannimiaineisto ja satunnaismetsäluokittelija liittyvät Turun yliopistoon keväällä 2025 tehtyyn pro gradu -tutkielmaan, jossa selvitettiin paikannimistön leksikaalisten viimeisten osien ja nimenalkujen alueellista variaatiota (linkki utupubiin tulossa). Tutkielmasta löytyy tarkempi selvitys, mutta lyhyesti sanottuna paikannimiä tarkasteltiin murrealueittain.

## Aineistot
Aineistoja on kolme: suomenkielisten maasto-, vesistö- ja asutusnimien aineisto (720 559 nimeä), murrealueittain tasattu aineisto (108 000 nimeä eli 13 500 nimeä kultakin murrealueelta) ja murrealueittain ja alaluokittain tasattu aineisto (108 000 nimeä eli 13 500 nimeä kultakin alueelta). Kaikissa aineistoissa on kaikista nimistä
1) paikannimi-ID (Id),
2) paikan koko nimi (spelling),
3) paikan laji Maanmittauslaitoksen koodina (placeTypeCode),
4) paikan sijaintikunta Maanmittauslaitoksen koodina (municipality),
5) tutkielmassa käytetyn murrealuejaottelun mukainen murrealuekoodi (murrealuekoodi),
6) tutkielmassa käytetyn murrealuejaottelun mukainen alaluokkakoodi (murrealaluokkakoodi),
7) paikannimistä erotetut yksikköön palautetut viimeiset leksikaaliset osat (leks_viim_yksikkö),
8) nimenalut (1 - 5 merkkiä nimen alusta muodossa alku_1, alku_2 jne.) ja
9) viimeistä osaa edeltävät epäodotuksenmukaiset merkit (erikoinen_merkki).

## Satunnaismetsäluokittelija-scripti
Scriptiin on sisällytetty kaikkien tarvittavien R-pakettien lataus ja tutkielmassa raportoitujen luokittelumallien muodostaminen. Scripti luo neljä erilaista satunnaismetsää: koko aineistoon perustuvan mallin, murrealueittain tasattuun aineistoon perustuvan paikanlajimallin, murrealueittain tasattuun aineistoon perustuvan nimenalkumallin ja murrealueittain ja alaluokittain tasattuun aineistoon perustuvan hybridimallin. Mallit on kuvattu tarkemmin tutkielmassa.
