# MongoDB Spark Connector 

The gma-coretechs fork of the [official MongoDB Spark Connector](https://github.com/mongodb/mongo-spark)

## Documentation

We created this fork to solve an issue with partitioning when Azure's cosmosdb doesn't return a non-zero average object size. It checks whether the value is positive and, if not, falls back to using the document count to partition

#### Official Docs:
See: https://docs.mongodb.com/spark-connector/

[API Documentation](https://www.javadoc.io/doc/org.mongodb.spark/mongo-spark-connector_2.11)

## Downloading
To use in a spark job

```
git clone https://github.com/gma-coretechs/mongo-spark
cd mongo-spark
sbt assembly
```

You can use the jar created in the target/scala-2.12 folder, passing it to your pyspark/spark-submit job with the --jars flag