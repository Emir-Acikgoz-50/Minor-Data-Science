## Data Visualization

Na dat ik de [Data Preparation]() voltooid had voor het SARIMA model diende ik het model om te gooien naar het verschil in aantal pakketten ten opzichte van de vorige dag in plaats van het werkelijke aantal pakketten, dit is gedaan om het model stationair te kunnen maken. Voor de uitvoering hiervan heb ik gebruik gemaakt van de volgende commando;

```
#Data Stationair maken
data_diff.plot()
```

Om het model zo efficiënt mogelijk te laten voorspellen, diende ik een keuze te maken hoe de data in een [Train, Validation & test set](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Notebook%20Bewijzen/train%20validate%20test%20set.PNG) gesplitst ging worden. De verdeling heb ik gedaan door middel van de volgende commando;

```
#Train, Validation & Test Split
from sklearn.model_selection import train_test_split

y = data_diff
X = data.index

train_size = 0.75
val_size = 0.25

split_index_val = int(data.shape[0]*(train_size-val_size))
split_index_test = int(data.shape[0]*train_size)

X_train = X[:split_index_val]
X_val = X[split_index_val:split_index_test]
X_test = X[split_index_test:]

y_train = y[:split_index_val]
y_val = y[split_index_val:split_index_test]
y_test = y[split_index_test:]

X_train_values = data[:split_index_val] # get the datetime values of X_train
X_val_values = data[split_index_val:split_index_test]
X_test_values = data[split_index_test:]
```
Omdat ik heb gefocust op de periode 2016-01-01 - 2020-01-01, heb ik gekozen om de eerste 2 jaar(2016-01-01 - 2018-01-01(60% van de data)) te gebruiken als Train set. In de train set wordt de data als het ware getraind in het model. De periode 2018-01-01 - 2019-01-01(20% van de data) gebruik ik voor de validatie set, binnen deze set wordt er getraind op ongeziene data en wordt de data beter getraind voor de uiteindelijke visualisatie. De periode 2019-01-01 - 2020-01-01, de overige 20% van de data, heb ik gebruikt voor de Test data, dit gedeelte wordt gebruikt als de ‘nieuwe’ data, om te zien hoe goed de voorspellingen het doen op data waarmee niet getraind is.




