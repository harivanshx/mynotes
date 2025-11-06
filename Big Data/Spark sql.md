
it is spark  for structured data processing
data frame and datasets 
[[Spark sql]] runs on top of of the [[spark core]]


Features 
- Integrated - Integrated with the other services of the spark
- Unified data access - it provide a single interface where you can query data from multiple sources
- High Compatibility - It is highly compatible with the [[hive table]]
- Standard Connectivity -  Means we can also connect with the java programs with jdbc/odbc
- Scalability- Apache Spark is big data technologies so we can easily expend or scale my cluster
- Performance Optimization - when we write sql query it will converted into logical path so it is optimized but also spark sql has something called catalyst optimizer and tungsten execution engine 



![[Pasted image 20250916115607.png]]

## Sql Context

Sql Context is a class used to initialize functionalities of spark sql




## [[Data frames]]

- Data frame is nothing but a distributed collection of data which is organized into named columns 
- A data frame can be constructed from an array of different sources such as tables , structured data files , external database or existing [[RDD]]
