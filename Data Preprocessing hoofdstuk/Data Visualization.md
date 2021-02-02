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


Om de configuratie van het SARIMA model te realiseren heb ik de volgende commando gebruikt(In het hoofdstuk [Configuring a model](https://github.com/Emir-Acikgoz-50/Minor-Data-Science/blob/main/Predictive%20Analytics%20Hoofdstuk/Configuring%20a%20model.md) staat duidelijk uitgelegd wat de configuratie inhoud en hoe het is uitgevoerd);

```
#Configuratie SARIMA Model
from statsmodels.tsa.statespace.sarimax import SARIMAX
my_order = (1,0,1)
my_seasonal_order = (0, 1, 1, 12)

``` 


In de volgende stap heb ik de Cross validatie techniek 'Rolling window'toegepast en vervolgens de uiteindelijke code voor het SARIMA model uitgevoerd, dit heb ik gedaan door middel van de volgende commando;

```
# Uitvoeren SARIMA + cross validatie : Rolling window
rolling_predictions = val_data.copy()
for train_end in val_data.index:
    train_data = y[:train_end-timedelta(days=1)]
    model = SARIMAX(train_data, order=my_order, seasonal_order=my_seasonal_order)
    model_fit = model.fit()
    
    pred = model_fit.forecast()
    rolling_predictions[train_end] = pred

```

```
rolling_residuals = val_data - rolling_predictions
```

Nadat de uitvoering van het model voltooid was heb ik het geplot en er een RMSE score bijgevoegd met de volgende commando;

```
#Plotten SARIMA + Metrics
plt.figure(figsize=(20,8))

plt.plot(y)
plt.plot(rolling_predictions)

plt.legend(('Data', 'Predictions'), fontsize=16)
plt.grid()
plt.xlabel('Datum',fontsize= 18)
plt.ylabel('Verschil Pakketten Vorige Dag',fontsize= 18)
plt.title('Rolling Window Validation Klant 266',fontsize= 18)
residuals = data_diff - model_fit.fittedvalues
print('Root Mean Squared Error:', np.sqrt(np.mean(residuals**2)))
```

De plot resulteerde in de [Visualisatie SARIMA model](), 


Toch wilde ik dat het stukje in de [visualisatie waar de voorspellingen zichbaar zijn]() duidellijk werdt, daarom heb ik een visualisatie ingezoomed op alleen de voorspellingen  met de volgende commando;

```
plt.figure(figsize=(20,8))

plt.plot(y['2018-01-01':'2019-01-01'])
plt.plot(rolling_predictions)

plt.legend(('Data', 'Predictions'), fontsize=16)
plt.grid()
plt.xlabel('Datum',fontsize= 18)
plt.ylabel('Aantal Pakketten',fontsize= 18)
plt.title('Rolling Window Validation Klant 266',fontsize= 18)
residuals = data_diff - model_fit.fittedvalues
print('Root Mean Squared Error:', np.sqrt(np.mean(residuals**2)))
```


