
Basic Type of Plot 
### 1.  Line Plot : Basic Plot for Numeric Data 

- For Time Series Models line plots are important
- It is just a 2D plot 
- Stock Prices 
- Dimensional Data 
- It is a 2D plot where multigraphs can be drawn by sharing the common x axis .
- On integrating with other graphs for generating twin y axis over the common x axis use the function twin x() where axis object has to be created . 
- For object oriented analysis , figure and axis objects are to be generated, where the same plot functions can now be instantiated  , invoked or call using the objects only , These are mainly used for 3D analysis or generating the new axis for the plots
- ==Object-Oriented Analysis (OOA) is the process of analyzing a problem domain to produce a conceptual model using objects, classes, and their relationships, expressed in terms of object-oriented concepts. It is the first phase in the Object-Oriented Analysis and Design (OOAD) lifecycle.==

- 


### 2.  Bar Chart: 

- For comparative analysis among different cat

- For analysis between numeric and discrete variable :
  - vertical Bar Chart (or plot) :
  - Horizontal Bar Chart : Used For Longer Group Label Names
	  - We use plt.barh function 
- Stacked Bar Plot is used to compare different parts of the entire representation 
- Grouped Bar Chart : This is used to provide the multiple analysis of different categories on the x axis which is distant seprated 
- PiChart : it is statistical circular distribution for a smaller range of data , where proportion in terms of percentage is evaluated to reflect the whole part relationship , Generally characterized by labels autopct and explode 
- Scatter Plot: A scatter plot is a set of points that represent the calues obtained for two different variables  plotted on a horizontal and vertival axis 
	- For bivariate analysis of numeric data 
	- Dependencies irrespective of the time
	- plt .scatter
	- sns.regplot
- 

- Histogram  : For numerical univariate analysis 


Categorical Data Plots : 
- Bar plots and count plots 
- These are used to study multiple categories over different types of estimated evaluators 
- Bar plots is generally associated with default mean value
- Also with the categorical Data plots , we use the  to add the another category




### Box Plot and violinplot are used 

where if the KDE Kernel Density Estimation is mainly analysed using violin plot 



- Cat Plot is a general plot for the categorical data where the kind parameter is used to provide the different types of plots 

# Distribution blocks

- For Uni variate  analysis  Dist plot is used
- Dist Plot and histogram are same 
- ### Joined Plot :
	- For bi variate analysis of the two numeric variables in terms of histogram 
	- This may Provide dist plot for univariate and scatter plot for bi variate
## KDE : plot
- To Study the probability distribution can be either pde function or kde function can be used with the univariate with the numeric variable , 

## Pair Plot :
- To study the pair wise relationship of the entire numeric column across the dataset, hue argument can be added to study one of the categorical columns


## Matrix Plot:
- Example : HeatMap
## Gridplot 
- Pair Plot and Facetgrid
- Grid Plots are used for the mapping multiple plots on rows and columns that can be generated on the grid layout 



## Regression Plot 

For bi variated analysis regplot will provided the best fitr line 
shaded area is confidence interval


Ln plot will provide regression plot on the faced grid , using rows , column ,hue




## 3D PLOT




For Clustering or for evaluating the geographical locations Geospatial Plot is used
Folium is one of the libraries that works with the map function characterized by latitude and longitude




	 
