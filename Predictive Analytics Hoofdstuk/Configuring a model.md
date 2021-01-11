## Configuring a model

**stationair uitleggen in jargon**

Binnen het TimeSerie model hebben we gefocut op vier verschillende methodes, maar om ook echt te weten op welke methode onze dataset past hebben we ze allemaal geconfigureerd en gevisualisseerd. Eerst begonnen we met een Simpel [Auto Regressive(AR)]() methode, vervolgens hebben we de Moving Average erbij gehaald [ARMA](), na deze methode hebben we het stationair gemaakt met het wel bekende [ARIMA]() methode, ten slotte werd het [SARIMA]() methode onder de loep genomen. Een verkeerde configuratie kan leiden tot verkeerde voorspellingen in de toekomst. Tijdens het configureren dient er reken gehouden te worden met de elementen p,d en q, deze elementen dienen toegepast te worden op de methode.

 voorbeeld ARIMA(train_data, (pdq))
p staat voor: Hoeveel orders er van een Auto Regressive methode wordt gebruikt
d staat voor: Hoeveel orders er stationair worden gemaakt
q staat voor: Hoeveel orders er van een Moving Average methode worden gebruikt

* Voor de AR methode wordt er niet gebruik gemaakt van de elementen
* Voor de MA methode worden alleen de elementen p en q gebruik gemaakt
* Voor de SARIMA methode komt er juist nog een s bij om een seizoen aan te geven.

Omdat er geen specifieke berekening is om de juiste configuratie te kiezen is er constant gespeeld met de getallen en is er gekozen om de volgende configuraties te kiezen


Om vervolgens de juiste methode te kiezen dient het model [geevalueert]() te worden.
