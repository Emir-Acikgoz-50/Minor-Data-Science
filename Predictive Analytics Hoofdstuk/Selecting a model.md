## Selecting a model

De dataset dat ik kreeg heb ik eerst bestudeerd en vervolgens [geplot](), de X-as was tijdsgebonden en op de Y-as stonden hoeveel pakketten er geleverd werden op een bepaalde dag. Na wat onderzoek te hebben gedaan op internet kwamen ik erachter dat voor dit tijdsgebonden data een dergelijke TimeSeries model goed uit kan pakken. Dit model heeft in totaal 11 verschillende soorten methodes om een voorspelling op te zetten.

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

Ik heb gekeken naar de [kenmerken,voordelen en nadelen]() per methode. Vanuit die informatie heb ik er voor gekozen om te focussen op de eerste vijf methodes voor dit onderzoek omdat deze het beste aansluiten bij de verkregen dataset. De methodes waar ik op gefocust heb zijn Autoregression (AR),Moving Average(MA), Auto Regression Moving Average(ARMA), Auto Regression Integrated Moving Average(ARIMA) en Seasonal Auto Regression Integrated Moving Average(SARIMA). Omdat de dataset seizoensgebonden is, heb ik er voor gekozen om uiteindelijk te focussen op een SARIMA methode.  Elke week heb ik een methode toegepast op de dataset en langamzer hand opgebouwd naar het SARIMA methode.
