

For converting categorical data into numerical data which is not ordinal we use the one hot encoding for that 

the main function of one hot encoding is to change the data into numeric values which are in the categorical values


to solve this we make some more column to get the data and we change the string into a vector dataset



![[Pasted image 20251202005105.png]]


Dummy variable trap : generally when we do one hot encoding after that we delete one column as because of multicolinearity as there should not be dependency of the input column as if you do work in linear models it can create a problem in the machine learning data 


![[Pasted image 20251202005318.png]]


we delete one column as we can also do it with the help of n-1 variable / column
![[Pasted image 20251202005426.png]]



for cars dataset 
Here brand is a nominal data 
then what we do is we just store the frequent data set of tables in this and delete 

