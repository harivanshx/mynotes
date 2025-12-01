

[[Machine Learning]]

we have to work with mostly csv files 
for the 90 percent of files 
and for 10 percent it is sql or json
or we also have apis or if we dont have any data then we find the data through web.scraping


- CSV : comma seprated values
- TSV : Tab Saparated values

```python

import pandas as pd


## Opening a local  csv file
df = pd.read_csv('aug_train.csv')

## Opening a csv file from an url 

import request 
from io import StringIO

url = ""
headers = {"User-Agent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:66/0 ) Gecko/20100101 Firefox/66.0"}
req = request.get(url, headers = headers)
data = StringIO(req.text)


pd.read_csv(data)
```


## Sep Parameter 

by default sep parameter is , but if we want to work with comma sep values then  we put sep as /t

```python
pd.read_csv('movie_titles_metadata.tsv', sep='\t',names=['sno','name','release_year' ,'rating' ,'votes' ,'genres' ])

```


## Index_col patameter



![[Pasted image 20251107215116.png]]

## Header parameter 

``` python
pd.read_csv('test.csv',header = 1)


```


![[Pasted image 20251107215254.png]]



## Use_cols parameters

```python
pd.read_csv('aug_train.csv', usecols = ['enrollee_id','gender','education_level'])



```


![[Pasted image 20251107215454.png]]

## Squeeze parameters 

```python
pd. read_csv('aug_train.csv', usecols=['gender' ], squeeze=True) 

```




## Skiprows/nrows



## Encoding Parameter

- to change the parameter from utf 8 to something else you can change it by changing the parameter of encoding 



## Skip bad lines

pd.read_csv(error_bad_lines = false)




## dtypes parameter 
 
- to change the data type we use the dtype parameter for that thing 
-  
![[Pasted image 20251107220013.png]]





## Handling Dates 

- When  we do read csv the date data become to sting then what we need to do from object to date time then we use parse_dates = ['Dates']
- ![[Pasted image 20251107220450.png]]



## Converters

![[Pasted image 20251107220619.png]]



![[Pasted image 20251107220607.png]]


## na_values parameter

![[Pasted image 20251107220828.png]]

here male becomes na value 

so we can define our own na values in the data frame so that it is easy to clean up the data


## loading a huge data set in chunks

- if we want to divide the dataset into chunks then what we need to is 
- ![[Pasted image 20251107221056.png]]
then we can use to get through the entre data
