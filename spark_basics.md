### Spark

#### History of Spark 

- 2009 - Started as a project at UC Berkley **AMPLab**
- 2010 - Open sourced under **BSD** license 
- 2013 - Spark became an Apache top level Project
- 2014 - Used by **Databricks** to sort large-scale datasets and set a new world record 

#### What is Apache Spark 

Apache Spark is an open-source distributed computing system designed to process and analyze large-scale datasets in a fast and efficient manner.

Support various programming languages - Python, Scala, R and Java 

Key features of Apache Spark include:
1. speed -  Leverages the distributed nature of the cluster to parallelize computations across multiple nodes, leading to high-speed data processing.
2. Ease of Use: Offers a simple and concise programming model that abstracts away the complexities of distributed computing, allowing developers to focus on their data processing tasks. 
3. Fault Tolerance: Spark automatically handles failures in distributed environments.
4. Scalability: Spark is designed to scale horizontally by adding more machines to the cluster. 
5. Versatility: Includes libraries for real-time streaming (Spark Streaming), interactive SQL queries (Spark SQL), machine learning (MLlib), and graph processing (GraphX).

#### Components of Spark 

1. Spark Core: Foundation of the Spark framework
    - Memory Management 
    - Fault Recovery
    - scheduling, distributing, and monitoring jobs on a cluster 
    - Interecting with storage system 
2. Spark SQL: Used for structured and semi-structured data processing 
3. Spark Streaming: A light-weight API that allows developers to perform batch processing and real time streaming of data with ease 
    - Provides secure, reliable, and fast processing of live data streams 
    - Input data stream -> Apache spark streaming -> Batches of input data -> Spark Engine -> Batches of processed data 
4. MLlib: MLlib is Spark's machine learning library, provides a rich set of machine learning algorithms and tools for tasks such as classification, regression, clustering, recommendation, and more. 
5. GraphX: Spark's own Graph computation engine and data store 
    - Provides a uniform tool for ETL 
    - Exploratory data analysis 
    - Interative graph compuations 
6. SparkR: SparkR is an R package that allows users to interact with Spark from the R programming language. It provides an R API for Spark, enabling data scientists and statisticians to leverage Spark's distributed computing capabilities using familiar R syntax and functions.
7. Cluster Manager: Spark can run on various cluster managers, including Apache Mesos, Hadoop YARN, and the standalone Spark cluster manager. The cluster manager is responsible for managing the allocation of cluster resources, coordinating task scheduling, and monitoring the health and performance of the Spark cluster.

#### Spark Job 

A Spark job refers to a specific computation or task that is submitted to the Spark cluster for execution. It represents a set of transformations and actions that are performed on the input data to achieve a desired outcome. 

1. Driver Program: The driver program is the entry point of a Spark application. It runs the main function and defines the SparkContext, which is responsible for coordinating the execution of the job. The driver program defines the sequence of transformations and actions to be performed on the data.
2. RDDs or DataFrames/Datasets: RDDs (Resilient Distributed Datasets) or DataFrames/Datasets are the distributed collections of data on which Spark jobs operate. RDDs are the fundamental data structures in Spark, while DataFrames and Datasets are higher-level abstractions that provide schema-awareness and optimization.
3. Transformations: Transformations are operations applied to RDDs or DataFrames/Datasets that create new RDDs or DataFrames/Datasets. Transformations are lazy, meaning they do not execute immediately but rather build a lineage of transformations that describe the computation. Examples of transformations include map, filter, groupBy, join, etc.
4. Actions: Actions are operations that trigger the execution of transformations and return results to the driver program or write data to an external system. Actions are eager and cause the evaluation of the RDD or DataFrame/Dataset lineage. Examples of actions include count, collect, reduce, save, etc.

When a Spark job is submitted, Spark analyzes the transformations and actions and optimizes their execution plan.

#### Spark's Structured API

- Spark's Structured API provides a user-friendly interface for working with structured data.
- It includes DataFrames, similar to tables, and Datasets, offering strong typing.
- DataFrames handle large-scale processing and support SQL-like queries, while Datasets bring type safety and object-oriented programming. Both allow data manipulation, filtering, aggregation, and joining.

#### Low-level API
- The low-level API in Spark provides control over RDDs, including data creation, partitioning, transformations, actions, fault tolerance, and iterative/interactive processing.
- It offers flexibility but requires handling lower-level details. Higher-level APIs like DataFrames and Datasets provide optimized abstractions for most use cases.














