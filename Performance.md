# Spark Performance

[**Glosario de Databricks**](https://www.databricks.com/glossary)

## General terms

[Apache Hive](https://www.databricks.com/glossary/apache-hive)
> Apache Hive is open-source data warehouse software designed to read, write, and manage large datasets extracted from the Apache Hadoop Distributed File System (HDFS) , one aspect of a larger Hadoop Ecosystem.

[Apache Spark](https://www.databricks.com/glossary/what-is-apache-spark)
>Apache Spark is an open source analytics engine used for big data workloads. It can handle both batches as well as real-time analytics and data processing workloads. Spark provides native bindings for the Java, Scala, Python, and R programming languages. It allows building applications for machine learning, stream processing, and graph processing. 


https://www.databricks.com/glossary/data-lakehouse

https://www.databricks.com/glossary/data-warehouse

## Specific terms

https://www.databricks.com/glossary/what-is-databricks-runtime

https://www.databricks.com/glossary/catalyst-optimizer

> At the core of Spark SQL is the Catalyst optimizer, which leverages advanced programming language features (e.g. Scala’s pattern matching and quasi quotes) in a novel way to build an extensible query optimizer. Catalyst is based on functional programming constructs in Scala and designed with these key two purposes:
> 1. Easily add new optimization techniques and features to Spark SQL
> 2. Enable external developers to extend the optimizer (e.g. adding data source specific rules, support for new data types, etc.)

![Catalyst Optimizer](https://www.databricks.com/wp-content/uploads/2018/05/Catalyst-Optimizer-diagram.png)

https://www.databricks.com/glossary/what-are-dataframes

>A DataFrame is a data structure that organizes data into a 2-dimensional table of rows and columns, much like a spreadsheet. DataFrames are one of the most common data structures used in modern data analytics because they are a flexible and intuitive way of storing and working with data.  Every DataFrame contains a blueprint, known as a schema, that defines the name and data type of each column. Spark DataFrames can contain universal data types like StringType and IntegerType, as well as data types that are specific to Spark, such as StructType. Missing or incomplete values are stored as null values in the DataFrame.


https://www.databricks.com/glossary/what-are-datasets

>Datasets are a type-safe version of Spark's structured API for Java and Scala. This API is not available in Python and R, because those are dynamically typed languages, but it is a powerful tool for writing large applications in Scala and Java. Recall that DataFrames are a distributed collection of objects of type Row, which can hold various types of tabular data. The Dataset API allows users to assign a Java class to the records inside a DataFrame, and manipulate it as a collection of typed objects, similar to a Java ArrayList or Scala Seq. The APIs available on Datasets are type-safe, meaning that you cannot accidentally view the objects in a Dataset as being of another class than the class you put in initially. This makes Datasets especially attractive for writing large applications where multiple software engineers must interact through well-defined interfaces. The Dataset class is parametrized with the type of object contained inside: Dataset in Java and Dataset[T] in Scala. As of Spark 2.0, the types T supported are all classes following the JavaBean pattern in Java, and case classes in Scala. These types are restricted because Spark needs to be able to automatically analyze the type T and create an appropriate schema for the tabular data inside your Dataset.

![Datasets](https://cms.databricks.com/sites/default/files/inline-images/datasets.png)
