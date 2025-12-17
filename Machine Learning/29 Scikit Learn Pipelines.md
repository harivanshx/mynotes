[[Machine Learning]]

Pipeline cgain togetger multiple steps so that the output of each step is used as input to the next step 
Pipelines mkaes it easy to apply the same preprocessing to train and test 

Pipelines chains together multiple steps so that the output of each step is used
as input to the next step.

Pipelines makes it easy to apply the same preprocessing to train and test!






``` python 



## titanic without using pipeline

import numpy as np
import pandas as pd

from sklearn.model_selection import train_test_split
from sklearn.impute import SimpleImputer
from sklearn.preprocessing import OneHotEncoder
from sklearn.preprocessing import MinMaxScaler
from sklearn.tree import DecisionTreeClassifier

df = pd.read_csv('train.csv')

df.head()



df.drop(columns=['PassengerId','Name','Ticket','Cabin'],inplace=True)

df.head()



X_train,X_test,y_train,y_test = train_test_split(df.drop(columns=['Survived']), df['Survived'], test_size=0.2, random_state=42)



  
X_train.head(2)




  
y_train.head()



  
df.isnull().sum()





X_train_embarked



  
one hot encoding Sex and Embarked ohe_sex = OneHotEncoder(sparse=False,handle_unknown='ignore') ohe_embarked = OneHotEncoder(sparse=False,handle_unknown='ignore') X_train_sex = ohe_sex.fit_transform(X_train[['Sex']]) X_train_embarked = ohe_embarked.fit_transform(X_train_embarked) X_test_sex = ohe_sex.transform(X_test[['Sex']]) X_test_embarked = ohe_embarked.transform(X_test_embarked)






```



![[Pasted image 20251216230047.png]]
