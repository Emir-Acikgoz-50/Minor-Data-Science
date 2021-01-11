## Training a model

Omdat we voor dit onderzoek gebruik hebben gemaakt van vier verschillende methodes, zijn er ook vier verschillende methodes geweest om de data te trainen.
Zoals eerder vermeld in het hoofdstuk over [data visualisation]() is de eerste 80% gebruikt voor het trainen van de data, hierbij ging het om de periode 2016-01-01 - 2018-01-01.
De Trainingset van 80% over de periode 2016-01-01 - 2018-01-01 geldt voor alle vier de methodes. De validatieset kreeg ook 10% en het overige 10% ging naar de testset. Om te voorkomen dat het model gaat underfitten en of overfitten is er gekozen om deze percentages te gebruiken.


* AR: `AR(train_data)`
* ARMA: `ARMA(train_data, AR, MA)`
* ARIMA: `ARIMA(train_data, AR, I, MA)`
* SARIMA: `SARIMAX(train_data, AR, I , MA, s)`

Omdat er uiteindelijk een SARIMA model uitgewerkt diende te worden, hebben we alleen op dit model gevalideerd. Binnen TimeSeries gebeurt het valideren door middel van een zo genoemde Rolling window. Binnen de techniek is de validatie niet altijd op een gelijk punt, maar verschuift het telkens. Dit is een validatie techniek die bij TimeSeries modellen wordt gebruikt, hiervan is gebruik  gemaakt om de data niet te laten under- of overfitten op de traingsset. Bij het uitvoeren van de techniek is er gekozen om binnen de periode 2016-01-01 - 2018-01-01 de data te trainen en pas in de periode 2018-01-01 - 2019-01-01 rolling window toe te passen. Hierbij wordt de training verlengd, dat wil zeggen dat er tot gisteren wordt getraind en voor morgen de validatie en test set van pas komt.



