



[[Machine Learning]]


Exporatory Data Analysis

- Univariate Analysis


we will only work on one variable 


#### Data  
- Numerical
- Categorical 


```python
import pandas as pd 
df = pd.read_csv('train.csv')
df.head()


```




 1. Categorigal Data 
a. Count plot

```python 
sns.countplot(df['survived'])
```


![[Pasted image 20251118094731.png]]




![[Pasted image 20251118094808.png]]

![[Pasted image 20251118094932.png]]


![[Pasted image 20251118095005.png]]
![[Pasted image 20251118095017.png]]
 



b. piechart

![[Pasted image 20251118095457.png]]

![[Pasted image 20251118095506.png]]


2. Numerical Data 


Histogram 


![[Pasted image 20251118111029.png]]
2.  Distplot

it also has kernal density estimation


![[Pasted image 20251118111113.png]]


3.  Box Plot


```Python 

sns.boxplot(df['Fare'])

```
![[Pasted image 20251118111532.png]]



