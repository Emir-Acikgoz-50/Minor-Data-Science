## Configuring a model


Binnen het TimeSerie model hebben we gefocust op vier verschillende methodes. Eerst begonnen we met een Simpel [Auto Regressive(AR)](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Codes/AR%20Model%20Klant%20266.ipynb) methode, vervolgens hebben we het uitgebreid met een Moving Average [ARMA](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Codes/ARMA%20Model%20Klant%20266.ipynb), daarna hebben we het model stationair gemaakt met het wel bekende [ARIMA](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Codes/Arima%20KLOPT%20100%25%20met%20zelf%20voorspelde%20eind.ipynb) methode, ten slotte zijn we begonnen aan het [SARIMA](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Codes/SARIMA_model_klant_266_rolling_window_verschil.ipynb) methode en die is uiteindelijk zo goed mogelijk geconfigureerd. Tijdens het configureren dient er reken gehouden te worden met de elementen P,D & Q deze elementen dienen toegepast te worden op de methode.

 *voorbeeld `SARIMA(train_data, (PDQs))`*
 
* P staat voor: Hoeveel orders er van een Auto Regressive methode wordt gebruikt
* D staat voor: Hoeveel orders er stationair worden gemaakt
* Q staat voor: Hoeveel orders er van een Moving Average methode worden gebruikt
* s staat voor: Geeft de lengte van de seizoenen aan( 12 is in dit geval een hele jaar)


 *Toepassing elementen op methodes

* Voor de AR methode wordt er niet gebruik gemaakt van de elementen
* Voor de MA methode worden alleen de elementen p en q gebruik gemaakt
* Voor de SARIMA methode komt er juist nog een s bij om een seizoen aan te geven.

Omdat er geen specifieke berekening is om de juiste configuratie te kiezen is er constant gespeeld met de getallen en is er gekozen om de volgende parameters te tunen en te gebruiken omdat deze de beste resultaten leverden.

* AR: `AR(train_data)`
* ARMA: `ARMA(train_data, 9, 10)`
* ARIMA: `ARIMA(train_data, 1, 1, 0)`
* SARIMA: `SARIMAX(train_data, 0, 1 , 1, 12)`

