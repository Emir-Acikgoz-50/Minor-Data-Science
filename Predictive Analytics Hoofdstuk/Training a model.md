## Training a model

Omdat we voor dit onderzoek gebruik hebben gemaakt van vier verschillende methodes, zijn er ook vier verschillende methodes geweest om de data te trainen.
Zoals eerder vermeld in het hoofdstuk over [data visualisation]() is de eerste 80% gebruikt voor het trainen van de data, hierbij ging het om de periode 2016-01-01 - 2018-01-01.
De Trainingset van 80% over de periode 2016-01-01 - 2018-01-01 geldt voor alle vier de methodes. De validatieset kreeg ook 10% en het overige 10% ging naar de testset. Om te voorkomen dat het model gaat underfitten en of overfitten is er gekozen om deze percentages te gebruiken.


* AR: `AR(train_data)`
* ARMA: `ARMA(train_data, AR, MA)`
* ARIMA: `ARIMA(train_data, AR, I, MA)`
* SARIMA: `SARIMAX(train_data, AR, I , MA, s)`
