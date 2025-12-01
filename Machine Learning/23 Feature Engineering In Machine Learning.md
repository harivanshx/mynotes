

![[Pasted image 20251119232656.png]]



![[Pasted image 20251119232736.png]]





### Feature Transformation 

- Missing Values Imputation  -- Work on by removing the or fill those missing values
- Handling Categorical Data - scikit learn only works over numerical data and don't work over the categorical data so what you need to do is convert that categorical data into numerical data by using the >>> One Hot Encoding
- Outliers Detection and removal --- ![[Pasted image 20251119234627.png]]
   ##########
- Feature Scaling - Get the data into same scale so that we can work on the process by scaling them together in a range generally -1 to 1



### Feature Construction 

- ![[Pasted image 20251119234832.png]]
we can see sibling and spouce and Parents child are both in family so can we add them up and add it to a new column named family so that it is so easy to understand and grab the knowledge out of it 
![[Pasted image 20251119235016.png]]


then we can get the feature family in categories


### Feature Selection 

- mnist dataset  have handwritten images of  digits 50000 images
- low res images 28 * 28
- white and black pixel
- so we can say 784 feature 
- but can we say all the 784 are important 
- we can reduce the dimension of the image so that we can get the data and also 
- reduce the number of features



### Feature Extraction 

- Rooms or Washrooms
- but we can use the sqft area as that feature directly dependent on the rooms and washrooms together 
- PCA is a most common feature extraction technique 

