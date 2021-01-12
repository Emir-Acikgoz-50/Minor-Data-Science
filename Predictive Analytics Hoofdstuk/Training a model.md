## Training a model

Omdat we voor dit onderzoek gebruik hebben gemaakt van vier verschillende methodes, zijn er ook vier verschillende methodes geweest om de data te trainen.
Zoals eerder vermeld in het hoofdstuk over [Data visualisation](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Data%20Preprocessing%20hoofdstuk/Data%20Visualization.md) is de eerste 80% gebruikt voor het trainen van de data, hierbij ging het om de periode 2016-01-01 - 2018-01-01.
De training set van 80% over de periode 2016-01-01 - 2018-01-01 geldt voor alle vier de methodes. De validatie set kreeg 10% van de data en de overige 10% ging naar de test set. Om te voorkomen dat het model gaat underfitten en/of overfitten is er gekozen om deze percentages te hanteren.


* AR: `AR(train_data)`
* ARMA: `ARMA(train_data, AR, MA)`
* ARIMA: `ARIMA(train_data, AR, I, MA)`
* SARIMA: `SARIMAX(train_data, AR, I , MA, s)`

Omdat er uiteindelijk een SARIMA model uitgewerkt diende te worden, hebben we alleen op dit model een cross validatie techniek gebruikt. Binnen TimeSeries gebeurt het valideren door middel van een zo genoemde [Rolling window](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Bewijzen/Code%20rolling%20window.PNG). Binnen de techniek is de validatie niet altijd op een gelijke punt, maar verschuift het telkens. Dit is een validatie techniek die bij TimeSeries modellen wordt gebruikt, hier is gebruik van gemaakt om de data niet te laten under- of overfitten op de traings set. Bij het uitvoeren van de techniek is er gekozen om binnen de periode 2016-01-01 - 2018-01-01 de data te trainen en pas in de periode 2018-01-01 - 2019-01-01 de rolling window toe te passen. Hierbij wordt de training verlengd, dat wil zeggen dat er tot gisteren wordt getraind en voor morgen de validatie en test set van pas komt.





