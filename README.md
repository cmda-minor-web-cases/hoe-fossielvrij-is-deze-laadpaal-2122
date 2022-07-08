# Hoe fossielvrij is deze laadpaal?

![Green Caravan](https://github.com/cmda-minor-web-cases/hoe-fossielvrij-is-deze-laadpaal/blob/main/assets/green-caravan.png?raw=true)

## Inhoudsopgave
  * [Beschrijving](#beschrijving)
  * [Opdrachtgever](#opdrachtgever)
  * [Design challenge](#design-challenge)
  * [Data](#data)
  * [Planning](#planning)
  * [Licentie](#licentie)

## Beschrijving
Nederland gaat in hoog tempo over op elektrisch rijden. Maar elektriciteit is nog niet fossielvrij. En met het laden van je elektrische auto stoot je dus CO2 uit. Hoeveel CO2 er vrijkomt hangt af
van waar, wanneer en natuurlijk hoeveel energie (kWh) je laadt. Dus hoe weet je hoeveel CO2 er vrijkomt als je je elektrische auto in een specifieke laadpaal plugt?

De Green Caravan heeft een datamodel ontwikkeld waarin energie-opwekking en -handel door heel Europa wordt gecombineerd met energie-mixen van energie-providers. Zo kun je tot op de laadpaal nauwkeurig opvragen hoeveel CO2, zon, wind, hydro, nucleair, kolen, gas en nog meer in een laadsessie zit. Green Caravan heeft niet alleen historische data, maar ook voorspellingen voor de nabije toekomst.

## Opdrachtgever
Green Caravan  
Product Owners: Tom Visser & Victor Zumpolle

## Design challenge
Ontwerp en ontwikkel een web applicatie die inzicht geeft in het gebruik van fossiele brandstoffen voor laadsessies van elektrische auto's

### User stories
**1. Fossiele elektriciteit uit laadpaal?**

Als elektrisch rijder,
wil ik weten hoeveel fossiele elektriciteit er uit de laadpaal komt waar ik naast sta, zodat ik weet hoe (on)duurzaam dat is.

Kunnen we deze data inzichtelijk maken en bijvoorbeeld via een QR-code op de laadpaal tonen?

**2 Beste laadpaal vinden**

Als elektrisch rijder,
wil ik graag weten bij welke laadpaal ik het meest duurzaam kan laden, zodat ik mijn auto zo duurzaam mogelijk oplaadt.

**3 Beste laadmoment bij laadpaal vinden**

Als elektrisch rijder,
wil ik graag weten op welk moment er het minste fossiele elektriciteit uit mijn laadpaal komt, zodat ik mijn auto zo duurzaam mogelijk oplaadt.

## Data
Green Caravan beschikt over meerdere datamodellen:  
* Exacte energie-mix van elektriciteit in Nederland, en bijbehorende CO2-emissies, tot op het uur nauwkeurig. Zowel historische data als voorspelling tot 48u in de toekomst.
* Contractuele energiemix per energie-provider in Nederland tot op het uur nauwkeurig. 

Deze time series data (en de laadsessies van de gebruikers) worden bijgehouden in een InfluxDB database. Deze heeft een eigen API en (JS) SDK en zal tijdens de meesterproef voor jullie beschikbaar gesteld worden. Door per laadpaal de informatie van de bijbehorende energie-provider te combineren met de data over de energie-mix kun je de exacte CO2-footprint van een laadsessie bij die laadpaal op
dat moment berekenen. We dagen je uit dit te realiseren en voor de gebruiker inzichtelijk te maken.

## Planning
In de eerste week van de meesterproef is een briefing met de opdrachtgever en begeleiders. Wekelijks wordt aan de opdrachtgever een prototype gedemonstreerd en de volgende stappen besproken. Tussentijds kunnen via Slack vragen gesteld worden.

Als agile studententeam krijgen jullie begeleiding van:  
* [Victor Zumpolle](https://www.linkedin.com/in/victor-zumpolle-52260b113), oud-CMD’er en nu front-ender bij De Voorhoede. Victor heeft 4 jaar geleden zelf de meesterproef gedaan en heeft gewerkt voor veel verschillende grote en kleine projecten binnen De Voorhoede. Hij zal jullie de nodige technische begeleiding geven. En als nodig staan ook de 20 front-end collega’s van Victor voor jullie klaar.
* [Tom Visser](tom.visser@gcrvn.com), product owner voor de software producten van Green Caravan. Tom stuurt nu het team aan dat de websites (greencrvn.com, www.co2smartcharging.com en
app.co2smartcharging.com) en de native apps (for Android en ioS) ontwikkelt.

De kickoff is maandag 23 mei om 14:00 uur te Voorhoede kantoor Amsterdam.
