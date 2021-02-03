## Selecting a model

De dataset dat ik kreeg heb ik eerst bestudeerd en vervolgens [geplot](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Bewijzen/plot%201.PNG), de X-as was tijdsgebonden en op de Y-as stonden hoeveel pakketten er geleverd werden op een bepaalde dag. Na wat onderzoek te hebben gedaan op internet kwamen ik erachter dat voor dit tijdsgebonden data een dergelijke TimeSeries model goed uit kan pakken. Dit model heeft in totaal 11 verschillende soorten methodes om een voorspelling op te zetten.

- Autoregression (AR)
- Moving Average (MA)
- Autoregressive Moving Average (ARMA)
- Autoregressive Integrated Moving Average (ARIMA)
- Seasonal Autoregressive Integrated Moving-Average (SARIMA)
- Seasonal Autoregressive Integrated Moving-Average with Exogenous Regressors (SARIMAX)
- Vector Autoregression (VAR)
- Vector Autoregression Moving-Average (VARMA)
- Vector Autoregression Moving-Average with Exogenous Regressors (VARMAX)
- Simple Exponential Smoothing (SES)
- Holt Winter’s Exponential Smoothing (HWES)

Ik heb gekeken naar de [kenmerken,voordelen en nadelen](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Screenshots%20Overig/Tijdreeks%20voorspellende%20modellen.pdf) per methode. Vanuit die informatie heb ik er voor gekozen om te focussen op de eerste vijf methodes voor dit onderzoek omdat deze het beste aansluiten bij de verkregen dataset. De methodes waar ik op gefocust heb zijn Autoregression (AR),Moving Average(MA), Auto Regression Moving Average(ARMA), Auto Regression Integrated Moving Average(ARIMA) en Seasonal Auto Regression Integrated Moving Average(SARIMA).
De gebruikte dataset was zowel trend- als seizoensgebonden, daarom vielen AR,MA, ARMA en ARIMA af en omdat de dataset seizoensgebonden is, heb ik er voor gekozen om uiteindelijk te focussen op een SARIMA methode. Echter heb ik elke week een methode toegepast op de dataset en langamzer hand opgebouwd naar het SARIMA methode.
