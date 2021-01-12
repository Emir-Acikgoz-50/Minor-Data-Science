## Data Visualization

Om het model zo efficiënt mogelijk te laten voorspellen, dient er een keuze gemaakt te worden hoe de data in een [Train, Validation & test set](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Bewijzen/train%20validate%20test%20set.PNG) gesplitst gaat worden.
Omdat er gefocust wordt over de periode 2016-01-01 - 2020-01-01, is er gekozen om de eerste 2 jaar(2016-01-01 - 2018-01-01(80%)) te gebruiken als Train set. In de train set wordt de data als het ware getraind in het model. De periode 2018-01-01 - 2019-01-01(10%) wordt gebruikt voor de validatie set, binnen deze set wordt er getraind op ongeziene data en wordt de data beter getraind voor de uiteindelijke visualisatie. De periode 2019-01-01 - 2020-01-01, de overige 10% van de data, dient gebruikt te worden voor de Test data, dit gedeelte wordt gebruikt als je ‘nieuwe’ data, om te zien hoe goed de voorspellingen het doen op data waarmee niet getraind is.

