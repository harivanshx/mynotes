

v[[Machine Learning]]





- Asking Basic Questions

![[Pasted image 20251118091759.png]]




How big is the data 

```python
df.shape

```

How does the data look like 

```python 
df.head()

# if you want to get the random sample from the data you will use the df.sample

df.sample()
```

What is the data type of cols()

```python

df.info()
```




Are there any missing values ????


```python 

df.isnull().sum()

```

How does the data look mathematically 


```python
df.describe

```

Are there duplicate values ???

```python

df.duplicated().sum()

```

How is the correlation between cols

```python 
df.corr()['survived']
```