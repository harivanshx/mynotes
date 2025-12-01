



[[Machine Learning]]



- json is used to get the data and this data is mainly available in data which we get from the 

![[Pasted image 20251107223132.png]]

```python
import pandas as pd
pd.read_json('recipie_test.json')
```



- Json is a universal format for storing data for non sql databases




```python
import pandas as pd
pd.read_json('https://api.github.com/users/hadley/orgs')
```


## Working with sql database
```python

!pip install mysql.connector


import mysql.connector
mysql.connector.connect(host = 'localhost',user = 'root', password = 'password', database = 'world')
pd.read_sql_query("select * from city",conn)




```
