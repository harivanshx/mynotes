
- Hadoop was the backbone of apache spark as hadoop comes first 
- Apache spark is also called in memory clustering platform
- Apache is 100 times faster because of processing of huge amount of data 

### Features   of Apache Spark 
1. [[fault tolerance ]]
2. [[Dynamic in nature ]]
3. [[Lazy Evaluation ]]
4. [[ Real time steam processing ]]
5. [[Reusability ]]
6. [[Speed]]
7. Advance [[Analysis]]
8. In Memory Computing 
- apache spark is an open source cluster computing framedfwork for real time data processing .

- main featue of apache spar in memory cluster computing that increase the processing speed of an application 

- Spark Provides an interface for programming entire cluste with inplicit data parallelism and fault tolerance 


### Components

##### Apache Core Api
- [[tags/Spark sql]] [[Database]] [[Database Management System]]
- [[Spark streaming]]
- [[Spark mlib]]
- [[Graphx]]
- [[SparkR]]



### [Resilient Distributed dataset] ([[RDD]])

[[RDD]] are the building blocks of any [[apache spark]] applications . Rdd stands for 
- Resilient [[fault tolerance]]  and is capable of rebuilding data on failure 
- Distributed : [[Distributed data]] among the multiple  nodes in a cluster 
- Dataset: Collection of partitioned data with values .

Rdd in a distrubuted dataset for the collection of the memory




### working with spark s=architecture




[[Flatmap]] : one to many transformation
	- Input = One parameter / one line (spark is fun)
	- output = many words ('spark','is','fun)



map does one to one transformation == that means input should be one and output will be one 


[[Lazy Evaluation]] 



[[DAG]]:  is nothing but just a graphical representation of [[linage]]

When the first time file is loaded from disk to memory it is called rdp 


[[cache()]] : the variable will stay for short '''it will help us in fault tolrance '''

[[persist()]] : the variable will stay for longer 






![[Pasted image 20250916105428.png]]




# [[Spark mlib]]
Spark Mlib is used to perform machine learning in Apache spark. 

Mlib Algorithms
-   Basics Statistics
- Classification and regression 
- Clustering 
- Dimesnioanl reduction 
- Feature Extraction

## Spark M Lib Tools
- ML Algorithms
- Featurization :
	- Converting Raw Data into Features
		- Tokenization 
- Pipelines:
	- When you are making the machine learning model by loading the data and saving the data into a pipeline 
- Persistence:
	- All the data Preprocessing and training steps are being embedded in pipeline
- Utilities:
	- Different models we are using in the machine learning model 
	- 

[[Event Time and Watermarking]] :
Event time is the timestamp when the data actually occurred, not when it arrived at spark for example a sensor may generate an event at 10 AM but spark may reeive it at 10:01

Why WaterMarking 
watermarking tell us 












[[Messaging System]]

Two types of Messaging System
- Messages are destributed ub a queue
- One or more consumers can consume the messages in the queue 
- Publish- Subscribe Messaging




Use Case of kafka
[[Messaging System]]

- Activity Tracking



![[Pasted image 20251103153414.png]]
A short description to identify your repository. If the repository is public, this description is used to index your content on Docker Hub and in search engines, and is visible to users in search results.

#### Visibility

Using 0 of 1 private repositories. [Get more](https://hub.docker.com/billing/core/purchase)

Public

Appears in Docker Hub search results

Private

Only visible to you

#### Pushing images

You can push a new image to this repository using the CLI:

docker tag local-image:tagname new-repo:tagname

docker push new-repo:tagname 