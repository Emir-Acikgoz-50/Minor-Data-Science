## Data Preparation

Om een zo helder en efficiënt mogelijke voorspelling te creëren heb ik me met de dataset gericht op klant 266 over de periode 2016-01-01 - 2020-01-01. 
Als eerst heb ik de benodigde pakketen ingeladen voor het uitvoeren van de commando's met het volgende commando;

```
# Import Packages
import pandas as pd
from pandas import datetime
from datetime import timedelta
import matplotlib.pyplot as plt
import numpy as np
import warnings; warnings.simplefilter('ignore')
```

Vervolgens heb ik de volledige data ingeladen in het model met de volgende commando;

```
# Read CSV file
df_postnl = pd.read_csv('/datc/parcel/notebooks/data/postnl/20201014_300_klanten.csv', parse_dates=[0], index_col=[0])
```

Omdat er bij PostNL in het weekend geen pakketten werden verwerkt en dit voor null waardes zorgt heb ik het weekend eruit gefilterd,Tevens om verdere problemen te voorkomen tijdens het modelleren, heb ik ook alle NaN waardes eruit gefilterd met de volgende commando;

```
cust_filter = data['cust_id'] == 'klant_266'
date_filter = data['procesdag'].dt.dayofweek <= 4
data = data.where(date_filter & cust_filter).dropna()
#data = data.where(cust_filter).dropna()

```

Om uiteindelijk alleen te focussen op de dataset van 2016-01-01 tot 2020-01-01 heb ik de volgende commando gebruikt om dat te realiseren;

```
data['procesdag']=pd.to_datetime(data['procesdag'])
data = data.set_index(data.procesdag, drop=True)
data = data['2016-01-01':'2020-01-01']
```
