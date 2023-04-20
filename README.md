# Practices - Data engineering

## TP - Data processing with Apache Spark
To process a large amount of data partitioned on a data lake, you can use data processing frameworks such as Apache Spark :
1. Read : https://spark.apache.org/docs/latest/sql-programming-guide.html

Some questions :
* What is Spark RDD API ?
  * Spark RDD (resilient distributed dataset) API is a tool that provides a way to manipulate a collection 
  of elements partitioned across the nodes of the cluster that can be operated on in parallel.
* What is Spark Dataset API ?
  * Spark Dataset API is a strongly-typed API that provides an object-oriented programming interface to work 
  with structured and semi-structured data using Spark.
* With which languages can you use Spark ? 
  * Spark can be used with Scala, Java, Python, and R.
* Which data sources or data sinks can Spark work with ?
  * File systems: HDFS, S3, local file system.
  * Relational databases: MySQL, PostgreSQL, Oracle, SQL Server. 
  * NoSQL databases: HBase, MongoDB.
  * Message brokers: Apache Kafka. 
  * Big Data frameworks: Apache HBase, Apache Cassandra, Apache Hive. 
  * Cloud storage services: Amazon S3, Google Cloud Storage, Azure Blob Storage.

### Analyse data with Apache Spark and Scala 
One engineering team of your company created for you a TV News data stored as JSON inside the folder `data-news-json/`.

Your goal is to analyze it with your savoir-faire, enrich it with metadata, and store it as [a column-oriented format](https://parquet.apache.org/).

1. Look at `src/main/scala/com/github/polomarcus/main/Main.scala` and update the code 

**Important note:** As you work for a top-notch software company following world-class practices, and you care about your project quality, you'll write a test for every function you write.

You can see tests inside `src/test/scala/` and run them with `sbt test`

### How can you deploy your app to a cluster of machines ?
* https://spark.apache.org/docs/latest/cluster-overview.html

### Business Intelligence (BI)
How could use we Spark to display data on a BI tool such as [Metabase](https://www.metabase.com/) ?

Tips: https://github.com/polomarcus/television-news-analyser#spin-up-1-postgres-metabase-nginxand-load-data-to-pg

### Continuous build and test
**Pro Tips** : https://www.scala-sbt.org/1.x/docs/Running.html#Continuous+build+and+test

Make a command run when one or more source files change by prefixing the command with ~. For example, in sbt shell try:
```bash
sbt
> ~ testQuick
```