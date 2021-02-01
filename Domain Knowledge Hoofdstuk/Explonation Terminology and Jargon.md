## Explonation Terminology and Jargon

**Om verwarring te voorkomen met de gebruikte vakjargon en terminologie binnen dit portfolio worden deze nader uitgelegd.** 

* Data Science

Gezien de snelle uitbreiding van het veld, kan het moeilijk zijn om de definitie van data science vast te stellen. In feite is het de discipline om gegevens en geavanceerde statistieken te gebruiken om voorspellingen te doen. Datawetenschap is ook gericht op het creëren van begrip tussen rommelige en ongelijksoortige data. Het 'wat' een onderzoeker aanpakt, zal binnen dit onderzoek gaan over het ontwikkelen van een systeem voor PostNL om een voorspelling te kunnen doen op het aantal binnenkomenden pakketene voor de volgende dag.


* Machine Learning

Machine Learning is de naam van het omvattende gebied van meerdere methoden waarbij de computer uitgerust wordt met ervaringen door patronen te herkennen in bestaande data, om met deze ervaring voorspellingen te kunnen doen op nieuwe data. Je hebt voor Machine Learning altijd een dataset nodig.

* Dataset

Een dataset is een verzameling gegevens. Een eenvoudig voorbeeld hiervan is een Excel spreadsheet. Hierin zijn gegevens verzameld in rijen en kolommen. Over het algemeen werk je met input data die voorspellende waarde heeft van hetgeen dat je wilt voorspellen, en met output data, hetgeen dat je wilt voorspellen. Voor dit onderzoek heb ik gebruik gemaakt van de dataset geleverd door PostNL, waarbij informatie beschikbaar was van 300 klanten over een periode van vijf jaar.

* Feature

Een features is een verzameling specifieke gegevens die je gebruikt om met Machine Learning model voorspellingen te doen. Dit is een van de input variabelen, ook wel de X-waarden genoemd. Denk hierbij bijvoorbeeld aan een tabel met eigenschappen van een huis. Een kolom met de oppervlakte zou hier een feature kunnen zijn. De output waarden zijn het resultaat van de voorspellingen die ook wel de y-waarden worden genoemd. Voor dit onderzoek zijn de volgende features gebruikt; Aantal pakketten, procesdag en klant ID.

* Algortime

Een algoritme is een rekenmethode. Dit kun je je voorstellen als een lijst coderegels die achtereenvolgens uitgevoerd worden. Er zijn verschillende Machine Learning algoritmes, die elk een eigen manier hebben om patronen in data vast te leggen.

* Trainen en testen

Trainen is het toepassen van een algoritme op een dataset waarbij het algoritme patronen herkent en vastlegt. Veelal gebruik je een bepaald gedeelte van je dataset (bijvoorbeeld 80%) om het algoritme mee te trainen, dit wordt traindata genoemd. Het overige gedeelte (de overige 20%) gebruik je als ‘nieuwe’ data, om te zien hoe goed je voorspellingen kunt doen op data waarmee niet getraind is, dit wordt testdata genoemd. Voor dit onderzoek is er 60% van de data voor training set gehanteerd en 20% voor het test set.

* Model

Wanneer een algoritme getraind is op een dataset en hiermee patronen heeft herkend en vastgelegd, is het resultaat een model. Waar een algoritme een universele reeks rekenregels omschrijft heeft een model zich aan een specifieke dataset aangepast en kan hiervoor voorspellingen doen. Tijdens dit onderzoek is er gebruik gemaakt van de modellen AR, MA, ARMA, ARIMA en SARIMA.

* Metrics

Metrics zijn de statistieken waarmee je de voorspellingsnauwkeurigheid van een model uit kunt drukken in een getal. Zo kun je bijvoorbeeld de nauwkeurigheid (accuracy) berekenen, hiermee verkrijg je het percentage juiste voorspellingen. Je vergelijkt dan bijvoorbeeld de accuracy van voorspellingen op de traindata met de accuracy van voorspellingen op de testdata. Zo krijg je een idee van hoe goed het model presteert op nieuwe ongeziene data. Tevens gebruik je metrics om het effect van aanpassingen inzichtelijk te maken. Voor dit onderzoek is er gebruik gemaakt van de R2 & RMSE metric score.


* Visualisatie

De visualisatie van de resultaten tijdens dit project werden gecreerd en getoond op de webiste Datascience.hhs.nl
Naast het verwerken en analyseren van grote hoeveelheden data, is de visualisatie van resultaten tijdens dit project  gecreerd en getoond op de webiste Datascience.hhs.nl. De tijden van het maken van lijn- en staafgrafieken in Excel lijken voor goed voorbij. Tools als Python beschikken over uitgebreide mogelijkheden om data te kunnen visualiseren.

* Python

Is een objectgeoriënteerde programmeertaal die vaak wordt gebruikt in data science omdat gebruikers een uitgebreide reeks tools hebben ontwikkeld die op het veld toepasbaar zijn. Python is gratis te gebruiken voor commerciële of persoonlijke projecten, en het wordt vaak geprezen om zijn leervermogen voor zowel programmeurs als niet-programmeurs.
Om deze taal te leren heb ik me verdiept op de courses van DataCamp.

* Overfitting

Overfitting gebeurt wanneer een model teveel informatie in overweging neemt. Het is alsof je iemand vraagt een zin te lezen terwijl hij door een microscoop naar een pagina kijkt. De patronen die het begrip mogelijk maken, gaan verloren in het ruis.

* Underfitting

Underfitting gebeurt wanneer er een model niet voldoende informatie biedt. Een voorbeeld van underfitting is iemand vragen om de temperatuurverandering over een dag in kaart te brengen en hem alleen de hoogste en laagste waarden te geven. In plaats van de vloeiende curve die je zou verwachten, heb je alleen voldoende informatie om een rechte lijn te trekken.

* Data Engineering

Bij data engineering draait alles om de back end. Voor ik aan de voorspellingen begon diende ik eerst de dataset te filteren en vergemakkelijken om de analyses uit te kunnen voeren.

* Feature Selection

Het proces om te bepalen welke eigenschappen van een dataset het meest waardevol zullen zijn bij het creeren van de modellen. Het is vooral handig bij onze grote dataset, omdat het gebruik van minder functies de hoeveelheid tijd en complexiteit vermindert die nodig is om een model te trainen en te testen. Het proces begint met het meten van hoe relevant elk kenmerk in een dataset is voor het voorspellen van het doelvariabele.

* Data Analysis

Deze analyse is het kleine broertje van data science. Data-analyse is meer gericht op het beantwoorden van vragen over heden en verleden. Het gebruikt minder complexe statistieken en probeert over het algemeen patronen te identificeren die PostNL als organisatie kan helpen verbeteren

* Time Series

Een tijdreeks is een set gegevens die is gesorteerd op het moment waarop elk gegevenspunt optrad. Denk aan de beurskoersen in de loop van een maand, of de temperatuur gedurende een dag. Ik heb me gefocust op de modellen AR, MA, ARMA, ARIMA en SARIMA van de Time Series methode.

 * Correlation
 
Correlatie is de maatstaf van hoeveel de ene set waardes van een andere afhangt. Als waardes samen toenemen, zijn ze positief gecorreleerd. Als de ene waarde van de ene set toeneemt naarmate de andere afneemt, zijn ze negatief gecorreleerd. Er is geen correlatie wanneer een verandering in de ene set niets te maken heeft met een verandering in de andere.

* Variatie

De variantie van een reeks waarden meet hoe verspreid die waarden zijn. Wiskundig gezien is het, het gemiddelde verschil tussen individuele waarden en het gemiddelde voor de reeks waarden. De wortel kwadraat van de variatie voor een set geeft ons de standaarddeviatie, die beter bruikbaar is.

* Root Mean Squared Error(RMSE)

RMSE is een maatstaf voor hoe verspreid de punten zijn. Met andere woorden, het vertelt hoe geconcentreerd de gegevens zijn rond de best passende lijn.

* Stationair

Tijdreeksen met trends of met seizoenen, zijn niet stationair -de trend en seizoensinvloeden zullen de waarde van de tijdreeksen op verschillende tijdstippen beïnvloeden. Daarom is het model stationair gemaakt. Dit diende te gebeuren bij de overstap van ARMA naar ARIMA 

* R2

R-kwadraat (R2) is een statistische maat die de proportie van de variantie voor een afhankelijke variabele vertegenwoordigt die wordt verklaard door een onafhankelijke variabele of variabelen in een regressiemodel.

* Neurale Netwerken

Een Machine Learning methode die heel losjes gebaseerd is op neurale verbindingen in de hersenen. Neurale netwerken is een systeem van verbonden knooppunten die zijn onderverdeeld in lagen: invoer-, uitvoer- en verborgen lagen. De verborgen lagen zijn de zware lifters die worden gebruikt om voorspellingen te doen. Waarden van de ene laag worden gefilterd door de verbindingen met de volgende laag, totdat de laatste set uitgangspunt is gegeven en een voorspelling is gedaan.


 
**Voor het Creeren van dit hoofdstuk is er gebruik gemaakt van de volgende middelen.**

| [Website 1](https://pythoncursus.nl/machine-learning-begrippen-termen/)|
|:---------:|
| [Website 2](https://www.springboard.com/blog/data-science-terms/#:~:text=At%20its%20essence%2C%20data%20science,%2C%20data%20mining%2C%20and%20programming.)|
| [Website 3](https://www.dataquest.io/blog/data-science-glossary/)|
 



















